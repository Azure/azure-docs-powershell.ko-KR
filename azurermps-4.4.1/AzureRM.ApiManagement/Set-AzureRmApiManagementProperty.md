---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
ms.openlocfilehash: 5273161b18f49e2cfd8f772987d8f0d9ce90bc69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525744"
---
# Set-AzureRmApiManagementProperty

## SYNOPSIS
API Management 속성을 수정 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Set-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tags <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmApiManagementProperty** Cmdlet은 Azure API Management 속성을 수정 합니다.

## 예제의

### 예제 1: 속성의 태그 변경
```
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

첫 번째 명령은 $Tags 변수에 두 개의 값을 할당 합니다.

두 번째 명령은 ID Property11를 가진 속성을 수정 합니다.
명령은 $Tags의 문자열을 속성의 태그로 할당 합니다.

### 예제 2: 비밀 값을 가질 수 있도록 속성 수정
```
PS C:\>Set-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property12" -Secret $True -PassThru
```

이 명령은 암호화 된 속성을 변경 합니다.

## 변수

### -컨텍스트
**PsApiManagementContext** 개체를 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
속성의 이름을 지정 합니다.
최대 길이는 100 자입니다.
이름에는 문자, 숫자, 마침표, 대시, 밑줄 문자만 포함 됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
이 cmdlet이이 cmdlet이 수정 하는 **PsApiManagementProperty** 를 반환 함을 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PropertyId
이 cmdlet이 수정 하는 속성의 ID를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -비밀
속성 값이 비밀 이며 암호화 되어야 함을 나타냅니다.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 태그
이 cmdlet이 속성에 연결 하는 태그의 배열을 지정 합니다.
태그를 사용 하 여 속성 목록을 필터링 할 수 있습니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -값
속성에 대 한 값을 지정 합니다.
이 값에는 정책 식이 포함 될 수 있습니다.
최대 길이는 1000 자입니다.
값이 비어 있거나 공백으로만 구성 되어 있지 않을 수 있습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

## 출력

### ApiManagement. ServiceManagement. \ PsApiManagementProperty

## 상속자

## 관련 링크

[Get-AzureRmApiManagementProperty](./Get-AzureRmApiManagementProperty.md)

[새로운 AzureRmApiManagementProperty](./New-AzureRmApiManagementProperty.md)

[제거-AzureRmApiManagementProperty](./Remove-AzureRmApiManagementProperty.md)


