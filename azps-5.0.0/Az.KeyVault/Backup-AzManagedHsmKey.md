---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
ms.openlocfilehash: 9e75b6de483f0103103434518d31b472660f4a70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304625"
---
# Backup-AzManagedHsmKey

## SYNOPSIS
관리 되는 HSM의 키를 백업 합니다.

## 구문과

### ByKeyName (기본값)
```
Backup-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByKey
```
Backup-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzManagedHsmKey** cmdlet은 관리 되는 HSM을 다운로드 하 여 파일에 저장 하 여 지정 된 키를 백업 합니다.
여러 버전의 키가 있는 경우 백업에 모든 버전이 포함 됩니다.
다운로드 된 콘텐츠는 암호화 되어 있으므로 Azure 관리 HSM 외부에서는 사용할 수 없습니다.
백업 된 구독에서 백업한 키를 관리 되는 HSM에 복원할 수 있습니다.
이 cmdlet을 사용 하는 일반적인 이유는 다음과 같습니다. 
- 관리 되는 HSM에서 실수로 키를 삭제 하는 경우 오프 라인 복사본을 사용할 수 있도록 키 복사본에 대해 에스크로 하려고 합니다.
 
- 관리 되는 HSM을 사용 하 여 키를 만들고, 이제 배포 된 응용 프로그램의 모든 인스턴스에서 사용할 수 있도록 해당 키를 다른 Azure 지역에 복제 하려고 합니다.
**AzManagedHsmKey** cmdlet을 사용 하 여 키를 암호화 된 형식으로 검색 한 다음 Restore-AzManagedHsmKey cmdlet을 사용 하 고 두 번째 지역에 관리 되는 HSM을 지정 합니다.

## 예제의

### 예제 1: 자동으로 생성 된 파일 이름으로 키 백업
```powershell
PS C:\Users\username\> Backup-AzManagedHsmKey -HsmName testmhsm -Name testkey

C:\Users\username\testmhsm-testkey-1602664728.7106073
```

이 명령은 testmhsm 이라는 관리 되는 HSM에서 testkey 라는 키를 검색 하 고 해당 키의 백업을 자동으로 이름이 지정 된 파일에 저장 하 고 파일 이름을 표시 합니다.

## 변수

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

### -Force
지정 된 파일 (있는 경우)을 덮어씁니다.

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

### -HsmName
HSM 이름. Cmdlet은 이름 및 현재 선택 된 환경에 따라 관리 되는 HSM의 FQDN을 생성 합니다.

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
검색할 키 번들로, 검색 호출의 출력에서 파이프라인으로 시작 합니다.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -이름
키 이름입니다.
Cmdlet은 관리 되는 HSM 이름, 현재 선택 된 환경 및 키 이름에서 키의 FQDN을 생성 합니다.

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
출력 파일입니다.
백업 된 키 blob을 저장할 출력 파일입니다.
표시 되지 않으면 기본 파일 이름이 선택 됩니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### Microsoft. KeyVault. PSKeyVaultKeyIdentityItem

## 출력

### System. 문자열

## 상속자

## 관련 링크

[추가-AzManagedHsmKey](./Add-AzManagedHsmKey.md)

[Get-AzManagedHsmKey](./Get-AzManagedHsmKey.md)

[제거-AzManagedHsmKey](./Remove-AzManagedHsmKey.md)

[실행 취소-AzManagedHsmKeyRemoval](./Undo-AzManagedHsmKeyRemoval.md)

[업데이트-AzManagedHsmKey](./Update-AzManagedHsmKey.md)

[Restore-AzManagedHsmKey](./Restore-AzManagedHsmKey.md)