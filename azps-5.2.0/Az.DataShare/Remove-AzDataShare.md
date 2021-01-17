---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 2679a3f63be3b7332020354e325e33573911334b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324337"
---
# Remove-AzDataShare

## SYNOPSIS
데이터 공유를 제거합니다.

## 구문

### ByFieldsParameterSet(기본값)
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByResourceIdParameterSet
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectParameterSet
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Remove-AzDataShare** cmdlet은 데이터 공유를 제거합니다.

## 예제

### 예제 1
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

이 명령은 Azure 데이터 공유 계정 WikiAds에서 AdsShare라는 데이터 공유를 제거합니다. 

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

### -AsJob
{{AsJob 설명 채우기}}

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
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

### -InputObject
Azure 데이터 공유 개체' ''yaml 형식: PSDataShare 매개 변수 집합: ByObjectParameterSet 별칭: 

필수: True 위치: 명명된 기본값: None Accept 파이프라인 입력: True(ByValue) Accept 와일드카드 문자: False

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Azure 데이터 공유 이름

yaml 형식: 문자열 매개 변수 집합: ByFieldsParameterSet 별칭: 

필수: True 위치: 명명된 기본값: None Accept 파이프라인 입력: False Accept 와일드카드 문자: False

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

### -PassThru
개체를 반환합니다(지정된 경우).

yaml 형식: SwitchParameter 매개 변수 집합: (모든) 별칭: 

필수: False 위치: 명명된 기본값: None Accept 파이프라인 입력: False Accept 와일드카드 문자: False

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Azure 데이터 공유 계정의 리소스 그룹 이름

yaml 형식: 문자열 매개 변수 집합: ByFieldsParameterSet 별칭: 

필수: True 위치: 명명된 기본값: None Accept 파이프라인 입력: False Accept 와일드카드 문자: False

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
Azure 데이터 공유의 리소스 ID

yaml 형식: 문자열 매개 변수 집합: ByResourceIdParameterSet 별칭: 

필수: True 위치: 명명된 기본값: None Accept 파이프라인 입력: True(ByPropertyName) Accept 와일드카드 문자: False

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

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

yaml 형식: SwitchParameter 매개 변수 집합: (모든) 별칭: cf

필수: False 위치: 명명된 기본값: None Accept 파이프라인 입력: False Accept 와일드카드 문자: False

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

yaml 형식: SwitchParameter 매개 변수 집합: (모든) 별칭: wi

필수: False 위치: 명명된 기본값: None Accept 파이프라인 입력: False Accept 와일드카드 문자: False




yaml 형식: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare 매개 변수 집합: ByObjectParameterSet 별칭:

필수: True 위치: 명명된 기본값: None Accept 파이프라인 입력: True(ByValue) Accept 와일드카드 문자: False

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare

## 출력

### System.Boolean

## 참고 사항

## 관련 링크
