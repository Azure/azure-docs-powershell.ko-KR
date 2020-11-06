---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: c337e82c88c7fdbbc1f8a3663249126c9d92b19f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536871"
---
# New-AzureRmApiManagementBackend

## SYNOPSIS
새 백엔드 엔터티를 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
Api Management에 새 백엔드 엔터티를 만듭니다.

## 예제의

### 기본 권한 부여 스키마를 사용 하 여 백엔드 123 만들기
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

새 백 엔드 만들기

## 변수

### -BackendId
새 백 엔드의 식별자입니다.
이 매개 변수는 선택 사항입니다.
지정 하지 않으면가 생성 됩니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -컨텍스트
PsApiManagementContext의 인스턴스입니다.
이 매개 변수는 필수입니다.

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Credential
백 엔드로 대화할 때 사용 해야 하는 자격 증명 세부 정보입니다.
이 매개 변수는 선택 사항입니다.

```yaml
Type: PsApiManagementBackendCredential
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -설명
백 엔드 설명입니다.
이 매개 변수는 선택 사항입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -프로토콜
백 엔드 통신 프로토콜.
이 매개 변수는 필수입니다.
유효한 값은 ' http ' 및 ' soap '입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -프록시
백 엔드에 요청을 보내는 동안 사용할 프록시 서버 세부 정보입니다.
이 매개 변수는 선택 사항입니다.

```yaml
Type: PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
외부 시스템 리소스의 관리 Uri입니다.
이 매개 변수는 선택 사항입니다.
이 url은 논리 앱, 함수 앱 또는 Api 앱의 Arm 리소스 Id 일 수 있습니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipCertificateChainValidation
백 엔드로 대화 하는 경우 인증서 체인 유효성 검사를 건너뛸지 여부
이 매개 변수는 선택 사항입니다.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipCertificateNameValidation
백 엔드로 대화 하는 경우 인증서 이름 유효성 검사를 건너뛸지 여부
이 매개 변수는 선택 사항입니다.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Title
백 엔드 제목.
이 매개 변수는 선택 사항입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Url
백 엔드의 런타임 Url입니다.
이 매개 변수는 필수입니다.

```yaml
Type: String
Parameter Sets: (All)
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
Type: SwitchParameter
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
Type: SwitchParameter
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

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### ApiManagement. ServiceManagement. \ PsApiManagementBackend

## 상속자

## 관련 링크

[Get-AzureRmApiManagementBackend](./Get-AzureRmApiManagementBackend)

[새로운 AzureRmApiManagementBackendCredential](./New-AzureRmApiManagementBackendCredential.md)

[새로운 AzureRmApiManagementBackendProxy](./New-AzureRmApiManagementBackendProxy.md)

[Set-AzureRmApiManagementBackend](./Set-AzureRmApiManagementBackend.md)

[제거-AzureRmApiManagementBackend](./Remove-AzureRmApiManagementBackend.md)

