---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
ms.openlocfilehash: 931ed484850654ecebc368ced0b378ce2a40944f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525595"
---
# Set-AzureRmVMAEMExtension

## SYNOPSIS
SAP 시스템에 대 한 모니터링 지원을 사용 하도록 설정 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Set-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-DisableWAD] [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmVMAEMExtension** cmdlet은 가상 컴퓨터에 설치 된 SAP 시스템에 대 한 모니터링 지원을 사용 하거나 업데이트 하도록 가상 컴퓨터의 구성을 업데이트 합니다.
Cmdlet은 성능 데이터를 수집 하 고 SAP 시스템을 검색할 수 있도록 하는 AEM (Azure 확장 모니터링) 확장을 설치 합니다.

## 예제의

### 예제 1: AEM extension 사용
```
PS C:\> Set-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

이 명령은 AEM 확장명을 사용 하도록 contoso-server 라는 가상 컴퓨터를 구성 합니다.
이 명령은 stdstorage 라는 저장소 계정을 지정 합니다.

## 변수

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

### -DisableWAD
이 cmdlet이 가상 컴퓨터에 대해 Azure 진단을 사용 하도록 설정 하지 않음을 나타냅니다.

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

### -EnableWAD
이 매개 변수를 제공 하면이 가상 컴퓨터에 대해 Windows Azure 진단을 사용 하도록 설정 됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -OSType
운영 체제 디스크의 운영 체제 유형을 지정 합니다.
운영 체제 디스크에 형식이 없는 경우이 매개 변수를 지정 해야 합니다.
이 매개 변수에 허용 되는 값은 Windows 및 Linux입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
이 cmdlet이 수정 하는 가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.

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

### -SkipStorage
이 cmdlet이 저장소 구성을 생략 했음을 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
가상 컴퓨터의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 AEM 확장을 추가 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WADStorageAccountName
이 cmdlet이 LinuxDiagnostics 또는 IaaSDiagnostics 확장을 구성 하는 데 사용 하는 저장소 계정의 이름을 지정 합니다.
가상 컴퓨터가 표준 저장소 계정을 사용 하지 않는 경우이 매개 변수에 대 한 값을 지정 해야 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-AzureRmVMAEMExtension](./Get-AzureRmVMAEMExtension.md)

[제거-AzureRmVMAEMExtension](./Remove-AzureRmVMAEMExtension.md)

[테스트-AzureRmVMAEMExtension](./Test-AzureRmVMAEMExtension.md)


