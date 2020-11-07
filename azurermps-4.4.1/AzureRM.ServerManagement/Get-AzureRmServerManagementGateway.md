---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: C579BF90-FD8B-4384-96EB-46154E308492
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
ms.openlocfilehash: 6b98f4266e730e1cfb60ef51046e6846f24999d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702691"
---
# Get-AzureRmServerManagementGateway

## SYNOPSIS
하나 이상의 서버 관리 게이트웨이를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### NoParams (기본값)
```
Get-AzureRmServerManagementGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Many-ByResourceGroup
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Single-ByName
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Single-ByObject
```
Get-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzureRmServerManagementGateway** cmdlet은 하나 이상의 Azure 서버 관리 게이트웨이를 가져옵니다.

## 예제의

### 예제 1: 구독에 있는 모든 게이트웨이 가져오기
```
PS C:\>Get-AzureRmServerManagementGateway
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
groupOne       centralus      Off          mygateway
groupOne       centralus      Off          othergateway
groupTwo       centralus      On           privategateway
```

이 명령은 구독에 있는 모든 서버 관리 게이트웨이를 가져옵니다.

### 예제 2: 리소스 그룹에서 게이트웨이 가져오기
```
PS C:\>Get-AzureRmServerManagementGateway -ResourceGroupName "Group001"
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
myGroup        centralus      Off          mygateway
```

이 명령은 Group001 이라는 리소스 그룹에 속하는 모든 서버 관리 게이트웨이를 가져옵니다.

### 예제 3: 설치 된 게이트웨이의 모든 인스턴스 가져오기
```
PS C:\>(Get-AzureRmServerManagementGateway -ResourceGroupName "Group002" -GatewayName "Gateway01").Instances
Name             Installed              Version         Operating System
----             ---------              -------         ----------------
GATEWAYPC        4/13/2016 6:35:04 PM   1.0.1104.0      Microsoft Windows 10 Enterprise
```

이 명령은 Group002 이라는 리소스 그룹에 속하는 Gateway01 이라는 서버 관리 게이트웨이의 모든 인스턴스를 가져옵니다.

## 변수

### -게이트웨이
이 cmdlet이 가져오는 게이트웨이를 지정 합니다.

Cmdlet은 지정 된 게이트웨이를 통해 *ResourceGroupName* 및 *게이트웨이 이름* 매개 변수를 사용 하 여 작업을 수행 합니다.

이 매개 변수를 지정 하면이 cmdlet에는 게이트웨이에 대 한 자세한 상태가 포함 됩니다.

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: Single-ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### --게이트웨이 이름
이 cmdlet이 게이트를 가져오는 서버 관리 게이트웨이의 이름을 지정 합니다.

않아도 *name* 매개 변수를 지정 하면이 cmdlet에는 게이트웨이에 대 한 자세한 상태가 포함 됩니다.

```yaml
Type: System.String
Parameter Sets: Single-ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
이 cmdlet이 게이트웨이를 가져오는 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: Many-ByResourceGroup, Single-ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 게이트웨이와
' Gateway ' 매개 변수는 파이프라인에서 ' Gateway ' 형식의 값을 허용 합니다.

## 출력

### Microsoft. ServerManagement. 모델 게이트웨이

## 상속자
* 매개 변수 없이이 cmdlet을 사용 하는 경우 구독과 연결 된 모든 게이트웨이가 반환 됩니다.

## 관련 링크

[새로운 AzureRmServerManagementGateway](./New-AzureRmServerManagementGateway.md)

[제거-AzureRmServerManagementGateway](./Remove-AzureRmServerManagementGateway.md)


