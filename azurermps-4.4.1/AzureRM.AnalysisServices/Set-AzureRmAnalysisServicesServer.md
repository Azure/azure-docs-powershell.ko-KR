---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 6bda63ad0c8e900a73c0ccd2afc506be7feae908
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525828"
---
# Set-AzureRmAnalysisServicesServer

## SYNOPSIS
Analysis Services 서버 인스턴스 수정

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### 기본값 (기본값)
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 백업 사용 안 함
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
Set-AzureRmAnalysisServicesServer cmdlet은 Analysis Services 서버의 인스턴스를 수정 합니다.

## 예제의

### 예제 1
```
PS C:\> Set-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

Resourcegroup에 대 한 testserver 라는 서버를 수정 하 여 태그를 key1로 설정 합니다. value1 및 key2: value2 및 관리자가 testuser1@contoso.com

## 변수

### -관리자
서버의 관리자로 설정할 사용자 또는 그룹의 쉼표로 구분 된 목록을 나타내는 문자열입니다.
사용자 또는 그룹에 UPN 형식 (예: 또는)을 지정 해야 합니다. user@contoso.comgroups@contoso.com

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BackupBlobContainerUri
Analysis Services 서버 백업용 blob 컨테이너 Uri

```yaml
Type: System.String
Parameter Sets: Default
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisableBackup
백업 blob 컨테이너를 사용 하지 않도록 전환 합니다.
백업 blob 컨테이너를 다시 사용 하도록 설정 하려면 백업 blob 컨테이너 Uri를-BackupBlobContainerUri로 제공 하세요.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable Backup
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
Analysis Services 서버의 이름입니다.

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

### -PassThru
작업이 성공적으로 완료 되 면 삭제 된 서버 세부 정보를 반환 합니다.

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
서버가 속한 Azure 리소스 그룹의 이름

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sku
서버의 Sku 이름입니다.
지원 되는 값은 표준 계층에 대 한 0 ', ' 1 ', ' 2 ', 4 '입니다. 기본 계층에 대 한 ' B1 ', ' B2 ', 개발 계층의 경우 1 '입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 태그
서버에서 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
사용자에 게 작업 수행 여부 확인 메시지 표시

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
현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.

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

## 출력

### AnalysisServicesServer를 통한 분석.

## 상속자
별칭: Set-AzureAs

## 관련 링크

[Get-AzureRmAnalysisServicesServer](./Get-AzureRmAnalysisServicesServer.md)

[제거-AzureRmAnalysisServicesServer](./Remove-AzureRmAnalysisServicesServer.md)
