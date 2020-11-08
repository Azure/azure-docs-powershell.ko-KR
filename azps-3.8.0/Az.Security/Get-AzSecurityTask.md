---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTask.md
ms.openlocfilehash: 9cdeb7d1640d3e92be2846ae73e8d8477feafd2a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041594"
---
# Get-AzSecurityTask

## SYNOPSIS
Azure 보안 센터에서 보안 환경을 강화 하기 위해 수행할 작업을 권장 하는 보안 작업을 가져옵니다.

## 구문과

### 구독 범위 (기본값)
```
Get-AzSecurityTask [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzSecurityTask -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelResource
```
Get-AzSecurityTask -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### 구독 Levelresource
```
Get-AzSecurityTask -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 리소스
```
Get-AzSecurityTask -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
Azure 보안 센터는 리소스를 검사 하 여 잠재적인 보안 문제를 검색 합니다.
이 cmdlet을 사용 하면 Azure 보안 센터에서 수행할 것을 권장 하는 보안 작업을 검색할 수 있습니다.

## 예제의

### 예제 1
```powershell
PS C:\> Get-AzSecurityTask
Id                                                                                                                                              Name                                 RecommendationType                                  ResourceId
--                                                                                                                                              ----                                 ------------------                                  ----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/08357a1e-c534-756f-cbb9-7b45e73f3137 08357a1e-c534-756f-cbb9-7b45e73f3137 Subscription has machines with failed baseline rule /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/0876feac-8c60-3fef-d95e-2c43b333ff14 0876feac-8c60-3fef-d95e-2c43b333ff14 Antimalware Health Issues                           /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/09ea0fa9-ce5a-d703-e17b-08f1d5246e2c 09ea0fa9-ce5a-d703-e17b-08f1d5246e2c Subscription has machines with failed baseline rule /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/11ff8541-820e-cecc-75de-91be7c0d8419 11ff8541-820e-cecc-75de-91be7c0d8419 Subscription has machines with failed baseline rule /subscriptions/48...
```

구독 내의 리소스에서 검색 된 모든 보안 작업을 가져옵니다.

### 예제 2
```powershell
PS C:\> Get-AzSecurityTask -ResourceGroupName "myService1"

Id                                                                                                                                                                        Name                                 RecommendationType                   ResourceI
                                                                                                                                                                                                                                                    d        
--                                                                                                                                                                        ----                                 ------------------                   ---------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/22ef553d-f13a-5227-ee4c-7cc861d28c96 22ef553d-f13a-5227-ee4c-7cc861d28c96 Enable DDoS protection standard      /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/47f736fa-0ec8-a372-de49-8cf18527930c 47f736fa-0ec8-a372-de49-8cf18527930c ConfigureTier2Waf                    /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/5696e90f-833d-494c-8833-f3be335fa9cb 5696e90f-833d-494c-8833-f3be335fa9cb NetworkSecurityGroupMissingOnVm      /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/65193cce-25a1-b30f-f94e-69d52e22923c 65193cce-25a1-b30f-f94e-69d52e22923c VulnerabilityAssessmentDeployment    /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/7e28a40d-e746-4751-8340-5126d6b77ae5 7e28a40d-e746-4751-8340-5126d6b77ae5 NetworkSecurityGroupMissingOnSubnet  /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/94867597-75e5-cfb6-8b71-e5e5253a24e1 94867597-75e5-cfb6-8b71-e5e5253a24e1 EncryptionOnVm                       /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/a02fffd5-1956-a6d7-73da-a87a65ae02f4 a02fffd5-1956-a6d7-73da-a87a65ae02f4 VulnerabilityAssessmentDeployment    /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/bd382d04-b478-ac77-e89f-300789032367 bd382d04-b478-ac77-e89f-300789032367 ProvisionNgfw                        /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/ce43626a-d56b-6a38-49ef-3ad7a731666e ce43626a-d56b-6a38-49ef-3ad7a731666e EncryptionOnVm                       /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/dcfb6365-799e-5ed4-f344-d86a0a4c2992 dcfb6365-799e-5ed4-f344-d86a0a4c2992 Enable auditing for the SQL database /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/ed736ed1-3f42-a95a-0b9e-458c44233937 ed736ed1-3f42-a95a-0b9e-458c44233937 Enable auditing for the SQL server   /subsc...
```

리소스 그룹 내의 리소스에서 검색 된 모든 보안 작업을 가져옵니다.

### 예제 3
```powershell
PS C:\> Get-AzSecurityTask -ResourceGroupName "myService1" -Name "22ef553d-f13a-5227-ee4c-7cc861d28c96"

Id                                                                                                                                                                        Name                                 RecommendationType              ResourceId    
--                                                                                                                                                                        ----                                 ------------------              ----------    
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/22ef553d-f13a-5227-ee4c-7cc861d28c96 22ef553d-f13a-5227-ee4c-7cc861d28c96 Enable DDoS protection standard /subscripti...
```

특정 보안 작업을 가져옵니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
리소스 이름입니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
리소스 ID입니다.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### Microsoft. Azure .의. PSSecurityTask. 작업

## 상속자

## 관련 링크
