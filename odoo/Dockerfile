FROM ursa/odoo-14.0:latest
MAINTAINER Open Source Integrators <support@opensourceintegrators.com>

# Copy files
COPY setup.py /odoo/
COPY migration.yml /odoo/

# Copy Odoo Addons
COPY src/private-addons /mnt/extra-addons/
# COPY src/enterprise /mnt/extra-addons/
# Add your module to the list below. Please respect the alphabetic order

COPY data /odoo/data
COPY songs /odoo/songs

RUN cd /odoo && pip3 install -r requirements.txt
RUN chown -R odoo /etc/odoo /mnt/extra-addons /odoo

USER odoo
