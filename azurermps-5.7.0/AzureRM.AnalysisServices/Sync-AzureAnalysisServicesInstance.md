---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: f3fb2377fd78db4b330afd39a8691f958597f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528159"
---
# Sync-AzureAnalysisServicesInstance

## SYNOPSIS

지정 된 Analysis Services 서버 인스턴스에서 지정 된 데이터베이스를 Add-AzureAnalysisServicesAccount 명령에 지정 된 현재 로그인 된 환경의 모든 query scaleout instance로 동기화 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-Passthru]
```

## 설명은

Sync-AzureAnalysisServicesInstance cmdlet은 지정 된 Analysis Services server 인스턴스의 지정 된 데이터베이스를 Add-AzureAnalysisServicesAccount 명령에 지정 된 대로 현재 로그인 한 환경의 모든 query scaleout instance로 동기화 합니다.

## 예제의

### 예제 1

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

이 명령은 사용자가 Add-AzureAnalysisServicesAccount 명령을 사용 하 여이 환경에 로그인 한 환경에서 ' contoso ' 라는 서버의 SalesOrders 데이터베이스를 동기화 합니다. westus.asazure.windows.net를 입력 합니다.

## 변수

### -인스턴스

다시 시작할 Analysis Services 서버 인스턴스의 이름

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -데이터베이스

동기화 할 데이터베이스의 id입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

명령이 성공적으로 실행 되 면 true를 반환 합니다.

```yaml
Type: Switch
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### 시스템 부울

## 상속자

별칭: Sync-AzureAsInstance

## 관련 링크
