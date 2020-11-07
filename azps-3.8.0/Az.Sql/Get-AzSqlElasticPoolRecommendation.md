---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
ms.openlocfilehash: 7e0d8e55b5a4ab3ab22081fde94bac10f4550730
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879637"
---
# Get-AzSqlElasticPoolRecommendation

## SYNOPSIS
탄력적 풀 추천 구성을 가져옵니다.

## 구문과

```
Get-AzSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzSqlElasticPoolRecommendation** cmdlet은 서버에 대 한 탄력적 풀 추천 구성을 가져옵니다.
이러한 권장 사항에는 다음 값이 포함 됩니다.
- DatabaseCollection. 풀에 속한 데이터베이스 이름의 모음입니다. 
- DatabaseDtuMin. 탄력적 풀의 데이터베이스에 대 한 DTU (데이터 전송 단위) 보장. 
 -- DatabaseDtuMax. 탄력적 풀의 데이터베이스에 대 한 DTU 캡입니다. 
- Dtu. 탄력적 풀에 대 한 DTU 보증입니다. 
- StorageMb 탄력적 풀의 저장소 (mb)입니다. 
- 평가판. 탄력적 풀 용 에디션. 이 매개 변수에 허용 되는 값은 Basic, Standard 및 Premium입니다. 
- IncludeAllDatabases. 탄력적 풀의 모든 데이터베이스가 반환 되는지 여부를 나타냅니다. 
- 성을. 탄력적 풀의 이름입니다.

## 예제의

### 예제 1: 서버에 대 한 권장 사항 보기
```
PS C:\>Get-AzSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

이 명령은 Server01 이라는 서버에 대 한 탄력적 풀 권장 사항을 가져옵니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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

### -ResourceGroupName
서버가 할당 된 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
이 cmdlet이 권장 사항을 제공 하는 서버의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

## 출력

### LegacySdk. UpgradeRecommendedElasticPoolProperties를 모두 보세요.

## 상속자

## 관련 링크
