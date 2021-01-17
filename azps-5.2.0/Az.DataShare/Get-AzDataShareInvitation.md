---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
ms.openlocfilehash: 0a723400bf92569a077abc64467c3cace56da0a6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350978"
---
# Get-AzDataShareInvitation

## SYNOPSIS
데이터 공유의 정보 초대를 얻습니다.

## 구문

### ByFieldsParameterSet(기본값)
```
Get-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByResourceIdParameterSet
```
Get-AzDataShareInvitation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzDataShareInvitation** cmdlet은 데이터 공유에 추가된 초대에 대한 정보를 얻습니다. 초대의 이름을 지정하면 이 cmdlet은 초대에 대한 정보를 얻습니다. 이름을 지정하지 않으면 이 cmdlet은 공유의 모든 초대에 대한 정보를 얻습니다.

## 예제

### 예제 1
```
PS C:\> Get-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation"

InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

이 명령은 데이터 공유 AdsShare에 있는 AdsInvitation 초대에 대한 정보를 제공합니다.

## PARAMETERS

### -AccountName
Azure 데이터 공유 계정 이름

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -Name
Azure 데이터 공유 초대 이름

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Azure 데이터 공유 계정의 리소스 그룹 이름

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Azure 데이터 공유 초대의 리소스 ID

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ShareName
Azure 데이터 공유 이름

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

## 출력

### Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare

## 참고 사항

## 관련 링크
