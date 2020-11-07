---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: b16e5a9ff2c6e5a898baf56cf237676665bc12c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696700"
---
# Remove-AzDataShare

## SYNOPSIS
데이터 공유를 제거 합니다.

## 구문과

### ByFieldsParameterSet (기본값)
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

## 설명은
**제거-AzDataShare** cmdlet은 데이터 공유를 제거 합니다.

## 예제의

### 예제 1
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

이 명령은 azure data share 계정 WikiAds에서 AdsShare 라는 데이터 공유를 제거 합니다. 

## 변수

### -AccountName
Azure data share 계정 이름

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
{{AsJob 입력 기술}}

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

### -InputObject
Azure data share 개체 ' ' ' yaml 유형: PSDataShare 매개 변수 집합: ByObjectParameterSet 별칭: 

필수: 실제 위치: 명명 된 기본값: 허용 파이프라인 입력 수락 안 함: True (ByValue) 와일드 카드 문자 허용: False


### -이름
Azure 데이터 공유 이름

yaml 유형: String 매개 변수 집합: ByFieldsParameterSet 별칭: 

필수: 실제 위치: 명명 된 기본값: 수락 파이프라인 입력 허용 안 함: False 와일드 카드 문자 허용: False


### -PassThru
Object (지정 된 경우)를 반환 합니다.

yaml 형식: SwitchParameter 매개 변수 집합: (All) 별칭: 

필수: False 위치: 명명 된 기본값: 허용 파이프라인 입력 수락 안 함: False 와일드 카드 문자 허용: False


### -ResourceGroupName
Azure data share 계정의 리소스 그룹 이름

yaml 유형: String 매개 변수 집합: ByFieldsParameterSet 별칭: 

필수: 실제 위치: 명명 된 기본값: 수락 파이프라인 입력 허용 안 함: False 와일드 카드 문자 허용: False


### -ResourceId
Azure data share의 리소스 id입니다.

yaml 유형: String 매개 변수 집합: ByResourceIdParameterSet 별칭: 

필수: 실제 위치: 명명 된 기본값: 없음 수락 파이프라인 입력: True (ByPropertyName) 와일드 카드 문자 허용: False


### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

yaml 형식: SwitchParameter 매개 변수 집합: (All) 별칭: cf

필수: False 위치: 명명 된 기본값: 허용 파이프라인 입력 수락 안 함: False 와일드 카드 문자 허용: False


### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

yaml 형식: SwitchParameter 매개 변수 집합: (All) 별칭: wi

필수: False 위치: 명명 된 기본값: 허용 파이프라인 입력 수락 안 함: False 와일드 카드 문자 허용: False
```

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

### -이름
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

### -PassThru
Object (지정 된 경우)를 반환 합니다.

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
Azure data share 계정의 리소스 그룹 이름

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
Azure data share의 리소스 id입니다.

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

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare

## 출력

### 시스템 부울

## 상속자

## 관련 링크
