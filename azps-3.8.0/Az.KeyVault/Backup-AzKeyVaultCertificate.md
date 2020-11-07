---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: 51d322ea738a56e4b1fa24cccdb7bb59a6cd0d21
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879266"
---
# <span data-ttu-id="ca33f-101">Backup-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ca33f-101">Backup-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="ca33f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca33f-102">SYNOPSIS</span></span>
<span data-ttu-id="ca33f-103">키 자격 증명 모음에서 인증서를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-103">Backs up a certificate in a key vault.</span></span>

## <span data-ttu-id="ca33f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ca33f-104">SYNTAX</span></span>

### <span data-ttu-id="ca33f-105">ByCertificateName (기본값)</span><span class="sxs-lookup"><span data-stu-id="ca33f-105">ByCertificateName (Default)</span></span>
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca33f-106">ByCertificate</span><span class="sxs-lookup"><span data-stu-id="ca33f-106">ByCertificate</span></span>
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca33f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ca33f-107">DESCRIPTION</span></span>
<span data-ttu-id="ca33f-108">**AzKeyVaultCertificate** cmdlet은 지정 된 인증서를 다운로드 하 고 파일에 저장 하 여 키 보관소에 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-108">The **Backup-AzKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="ca33f-109">인증서에 여러 버전이 있으면 모든 버전이 백업에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="ca33f-110">다운로드 된 콘텐츠는 암호화 되어 있으므로 Azure 키 자격 증명 모음 외부에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="ca33f-111">인증서가 백업 된 구독의 모든 키 보관소 (자격 증명 모음이 동일한 Azure 지리에 있는 경우)로 복구 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="ca33f-112">이 cmdlet을 사용 하는 일반적인 이유는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="ca33f-113">자격 증명 모음에서 원본을 실수로 삭제 한 경우에 대비 하 여 인증서의 오프 라인 복사본을 유지 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="ca33f-114">키 자격 증명 모음을 사용 하 여 인증서를 만든 후 분산 응용 프로그램의 모든 인스턴스에서 사용할 수 있도록 개체를 다른 Azure 지역에 복제 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="ca33f-115">**AzKeyVaultCertificate** cmdlet을 사용 하 여 암호화 된 형식으로 인증서를 검색 한 다음 **Restore-AzKeyVaultCertificate** cmdlet을 사용 하 고 두 번째 지역에서 키 자격 증명 모음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-115">Use the **Backup-AzKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="ca33f-116">예제의</span><span class="sxs-lookup"><span data-stu-id="ca33f-116">EXAMPLES</span></span>

### <span data-ttu-id="ca33f-117">예제 1: 자동으로 생성 된 파일 이름으로 인증서 백업</span><span class="sxs-lookup"><span data-stu-id="ca33f-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="ca33f-118">이 명령은 MyKeyVault 이라는 키 자격 증명 모음에서 MyCert 이라는 인증서를 검색 하 고, 해당 인증서의 백업을 자동으로 이름이 지정 된 파일에 저장 하 고, 파일 이름을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="ca33f-119">예제 2: 인증서를 지정 된 파일 이름으로 백업</span><span class="sxs-lookup"><span data-stu-id="ca33f-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="ca33f-120">이 명령은 MyKeyVault 이라는 키 자격 증명 모음에서 MyCert 이라는 인증서를 검색 하 고 해당 인증서의 백업을 blob 라는 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="ca33f-121">예제 3: 이전에 검색 한 인증서를 지정 된 파일 이름으로 백업 하 고 메시지를 표시 하지 않고 대상 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="ca33f-122">이 명령은 $cert 라는 인증서의 백업을 만듭니다. $Cert의 자격 증명 모음에 이름으로 지정 합니다. VaultName 파일에 이미 있는 경우 파일을 자동으로 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="ca33f-123">변수</span><span class="sxs-lookup"><span data-stu-id="ca33f-123">PARAMETERS</span></span>

### <span data-ttu-id="ca33f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca33f-124">-DefaultProfile</span></span>
<span data-ttu-id="ca33f-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca33f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="ca33f-126">-Force</span></span>
<span data-ttu-id="ca33f-127">지정 된 파일 (있는 경우)을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="ca33f-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca33f-128">-InputObject</span></span>
<span data-ttu-id="ca33f-129">백업할 비밀을 검색 호출의 출력에서 파이프라인으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByCertificate
Aliases: Certificate

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca33f-130">-이름</span><span class="sxs-lookup"><span data-stu-id="ca33f-130">-Name</span></span>
<span data-ttu-id="ca33f-131">비밀 이름.</span><span class="sxs-lookup"><span data-stu-id="ca33f-131">Secret name.</span></span>
<span data-ttu-id="ca33f-132">Cmdlet은 자격 증명 정보, 현재 선택 된 환경 및 비밀 이름 으로부터 비밀의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca33f-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="ca33f-133">-OutputFile</span></span>
<span data-ttu-id="ca33f-134">출력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-134">Output file.</span></span>
<span data-ttu-id="ca33f-135">인증서 백업을 저장할 출력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="ca33f-136">지정 하지 않으면 기본 파일 이름이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-136">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="ca33f-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ca33f-137">-VaultName</span></span>
<span data-ttu-id="ca33f-138">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="ca33f-138">Vault name.</span></span>
<span data-ttu-id="ca33f-139">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca33f-140">-확인</span><span class="sxs-lookup"><span data-stu-id="ca33f-140">-Confirm</span></span>
<span data-ttu-id="ca33f-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca33f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca33f-142">-WhatIf</span></span>
<span data-ttu-id="ca33f-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca33f-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca33f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca33f-145">CommonParameters</span></span>
<span data-ttu-id="ca33f-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca33f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca33f-147">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ca33f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca33f-148">입력</span><span class="sxs-lookup"><span data-stu-id="ca33f-148">INPUTS</span></span>

### <span data-ttu-id="ca33f-149">Microsoft. KeyVault. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ca33f-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="ca33f-150">출력</span><span class="sxs-lookup"><span data-stu-id="ca33f-150">OUTPUTS</span></span>

### <span data-ttu-id="ca33f-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ca33f-151">System.String</span></span>

## <span data-ttu-id="ca33f-152">상속자</span><span class="sxs-lookup"><span data-stu-id="ca33f-152">NOTES</span></span>

## <span data-ttu-id="ca33f-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca33f-153">RELATED LINKS</span></span>
