---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://go.microsoft.com/fwlink/?LinkId=690160
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
ms.openlocfilehash: 28cd93fe9de14365e4de626729ec45a7aaa88cdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537155"
---
# New-AzureRmKeyVault

## SYNOPSIS
키 자격 증명 모음을 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureRmKeyVault [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
**AzureRmKeyVault** cmdlet은 지정 된 리소스 그룹에 키 자격 증명 모음을 만듭니다. 또한이 cmdlet은 현재 로그온 한 사용자에 게 키 자격 증명 모음에서 키와 비밀을 추가, 제거 또는 나열할 수 있는 권한을 부여 합니다.

참고: 새 키 자격 증명 모음을 만들려고 할 때 **구독이 ' microsoft. KeyVault '을 사용 하도록 등록 되어 있지 않은** 경우 **AzureRmResourceProvider-Providernamespace "Microsoft. keyvault"** 을 실행 한 다음 **새-AzureRmKeyVault** 명령을 다시 실행 하세요. 자세한 내용은 Register-AzureRmResourceProvider를 참조 하세요.

## 예제의

### 예제 1: 표준 키 보관소 만들기
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

이 명령은 Azure 지역 동부 US에 Contoso03Vault 이라는 키 자격 증명 모음을 만듭니다. 이 명령은 Group14 이라는 리소스 그룹에 키 보관소를 추가 합니다. 명령이 *SKU* 매개 변수에 대 한 값을 지정 하지 않기 때문에 표준 키 자격 증명 모음이 만들어집니다.

### 예제 2: Premium 키 자격 증명 모음 만들기
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

이 명령은 이전 예제와 마찬가지로 키 자격 증명 모음을 만듭니다. 그러나, Premium 키 자격 증명 모음을 만들기 위해 *SKU* 매개 변수에 premium 값을 지정 합니다.

## 변수

### -EnabledForDeployment
이 키 자격 증명 모음이 리소스 만들기에서 참조 되는 경우 (예: 가상 컴퓨터를 만들 때)이 키 보관소에서 비밀을 검색 하도록 Microsoft. a 리소스 공급자를 설정 합니다.

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

### -EnabledForDiskEncryption
Azure 디스크 암호화 서비스에서이 키 자격 증명 모음의 비밀 및 래핑 키를 가져올 수 있도록 합니다.

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

### -EnabledForTemplateDeployment
이 키 자격 증명 모음이 서식 파일 배포에서 참조 되는 경우 Azure 리소스 관리자가이 키 보관소에서 비밀을 가져올 수 있도록 합니다.

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

### -EnableSoftDelete
지정 된 경우이 키 보관소에 대해 ' 소프트 삭제 ' 기능을 사용할 수 있습니다.

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

### -위치
키 자격 증명 모음을 만들 Azure 지역을 지정 합니다. 명령 Get-AzureLocation ( https://msdn.microsoft.com/ library/azure/mt589064)을 사용 하 여 선택 항목을 확인 합니다. 자세한 내용은을 입력 `Get-Help Get-AzureLocation` 하세요.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
키 자격 증명 모음을 만들 기존 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sku
키 보관소 인스턴스의 SKU를 지정 합니다. 각 SKU에 대해 사용할 수 있는 기능에 대 한 자세한 내용은 Azure 키 보관소 가격 웹 사이트 ()를 참조 하세요 https://go.microsoft.com/fwlink/?linkid=512521) .

```yaml
Type: Microsoft.Azure.Management.KeyVault.Models.SkuName
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 태그
해시 테이블 형태의 키-값 쌍입니다. 예를 들어:

@ {key0 = "value0", key1 = $null, key2 = "value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
만들려는 키 보관소의 이름을 지정 합니다. 이름은 문자, 숫자 또는 하이픈을 임의로 조합 하 여 사용할 수 있습니다. 이름은 문자 또는 숫자로 시작 하 고 끝나야 합니다. 이름은 범용으로 고유 해야 합니다.

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
Default value: None
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

### Microsoft. KeyVault. PSVault

## 상속자

## 관련 링크

[Get-AzureRmKeyVault](./Get-AzureRmKeyVault.md)

[제거-AzureRmKeyVault](./Remove-AzureRmKeyVault.md)
