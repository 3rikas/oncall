# Grafana OnCall

Developer-friendly, incident response management with brilliant Slack integration.
- Collect and analyze alerts from multiple monitoring systems
- On-call rotations based on schedules
- Automatic escalations
- Phone calls, SMS, Slack, Telegram notifications

![Grafana OnCall Screenshot](screenshot.png)

## Getting Started

### Production environment

For production setup check [PRODUCTION.md](PRODUCTION.md).

### Hobby environment

Download docker-compose.yaml:
```bash
curl https://github.com/... -o docker-compose.yaml
```

Set environment:
```bash
export DOMAIN=http://localhost
export SECRET_KEY=my_random_secret_must_be_more_than_32_characters_long
export RABBITMQ_PASSWORD=rabbitmq_secret_pw
export MYSQL_PASSWORD=mysql_secret_pw
export COMPOSE_PROFILES=with_grafana
export GRAFANA_USER=admin
export GRAFANA_PASSWORD=admin
```

Launch services:
```bash
docker-compose -f docker-compose.yml up --build -d
```

Issue invite token and get further instructions:
```bash
docker-compose -f docker-compose.yml run engine python manage.py issue_invite_for_the_frontend --override
```

## Join our community 👋

<table>
  <tbody>
    <tr>
      <td><a href=""><img src="docs/img/community_call.png"></a></td>
      <td><a href=""><img src="docs/img/community_call.png"></a></td>
      <td><a href=""><img src="docs/img/community_call.png"></a></td>
    </tr>
  </tbody>
</table>

## Further Reading
- *Documentation* - [Grafana OnCall](https://grafana.com/docs/grafana-cloud/oncall/)
- *Blog Post* - [Announcing Grafana OnCall, the easiest way to do on-call management](https://grafana.com/blog/2021/11/09/announcing-grafana-oncall/)
- *Presentation* - [Deep dive into the Grafana, Prometheus, and Alertmanager stack for alerting and on-call management](https://grafana.com/go/observabilitycon/2021/alerting/?pg=blog)
