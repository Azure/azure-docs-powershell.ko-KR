---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: e4692d9b623ce285a2be50d51a450fd8da39a5ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968960"
---
# <span data-ttu-id="9ea70-101">Backup-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="9ea70-101">Backup-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="9ea70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ea70-102">SYNOPSIS</span></span>
<span data-ttu-id="9ea70-103">키 자격 증명 모음에 인증서를 백업합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-103">Backs up a certificate in a key vault.</span></span>

## <span data-ttu-id="9ea70-104">구문</span><span class="sxs-lookup"><span data-stu-id="9ea70-104">SYNTAX</span></span>

### <span data-ttu-id="9ea70-105">ByCertificateName(기본값)</span><span class="sxs-lookup"><span data-stu-id="9ea70-105">ByCertificateName (Default)</span></span>
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ea70-106">ByCertificate</span><span class="sxs-lookup"><span data-stu-id="9ea70-106">ByCertificate</span></span>
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ea70-107">설명</span><span class="sxs-lookup"><span data-stu-id="9ea70-107">DESCRIPTION</span></span>
<span data-ttu-id="9ea70-108">**Backup-AzKeyVaultCertificate** cmdlet은 키 자격 증명 모음에 지정된 인증서를 다운로드하고 파일에 저장하여 백업합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-108">The **Backup-AzKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="9ea70-109">인증서에 여러 버전이 있는 경우 모든 버전이 백업에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="9ea70-110">다운로드한 콘텐츠는 암호화되어 있기 때문에 Azure Key Vault 외부에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="9ea70-111">자격 증명 모음이 동일한 Azure 지리에 있는 경우 백업된 인증서를 백업된 구독의 모든 키 자격 증명 모음에 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="9ea70-112">이 cmdlet을 사용하는 일반적인 이유는 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="9ea70-113">자격 증명 모음에서 실수로 원본을 삭제하는 경우 인증서의 오프라인 복사본을 유지하려는 경우.</span><span class="sxs-lookup"><span data-stu-id="9ea70-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="9ea70-114">Key Vault를 사용하여 인증서를 만들었다가 이제 개체를 다른 Azure 지역으로 복제하여 분산된 애플리케이션의 모든 인스턴스에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="9ea70-115">**Backup-AzKeyVaultCertificate** cmdlet을 사용하여 암호화된 형식으로 인증서를 검색한 다음 **Restore-AzKeyVaultCertificate** cmdlet을 사용하여 두 번째 지역에서 키 자격 증명 모음을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-115">Use the **Backup-AzKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="9ea70-116">예제</span><span class="sxs-lookup"><span data-stu-id="9ea70-116">EXAMPLES</span></span>

### <span data-ttu-id="9ea70-117">예제 1: 자동으로 생성된 파일 이름으로 인증서 백업</span><span class="sxs-lookup"><span data-stu-id="9ea70-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="9ea70-118">이 명령은 MyKeyVault라는 키 자격 증명 모음에서 MyCert라는 인증서를 검색하고 해당 인증서의 백업을 자동으로 이름이 지정된 파일에 저장하고 파일 이름을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="9ea70-119">예제 2: 지정된 파일 이름으로 인증서 백업</span><span class="sxs-lookup"><span data-stu-id="9ea70-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="9ea70-120">이 명령은 MyKeyVault라는 키 자격 증명 모음에서 MyCert라는 인증서를 검색하고 해당 인증서의 백업을 Backup.Blob이라는 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="9ea70-121">예제 3: 이전에 검색한 인증서를 지정된 파일 이름으로 백업하여 메시지가 표시되지 않고 대상 파일을 덮어 덮어 덮어 니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="9ea70-122">이 명령은 인증서라는 인증서의 백업을 $cert. 자격 증명 모음의 이름은 $cert. Backup.blob이라는 파일로 VaultName을 지정하여 파일이 이미 있는 경우 파일을 자동으로 덮어 덮어 봅니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="9ea70-123">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9ea70-123">PARAMETERS</span></span>

### <span data-ttu-id="9ea70-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ea70-124">-DefaultProfile</span></span>
<span data-ttu-id="9ea70-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ea70-126">-Force</span><span class="sxs-lookup"><span data-stu-id="9ea70-126">-Force</span></span>
<span data-ttu-id="9ea70-127">해당 파일이 있는 경우 주어진 파일을 덮어 덮어 덮어</span><span class="sxs-lookup"><span data-stu-id="9ea70-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="9ea70-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ea70-128">-InputObject</span></span>
<span data-ttu-id="9ea70-129">검색 호출의 출력에서 백업할 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="9ea70-130">-Name</span><span class="sxs-lookup"><span data-stu-id="9ea70-130">-Name</span></span>
<span data-ttu-id="9ea70-131">비밀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-131">Secret name.</span></span>
<span data-ttu-id="9ea70-132">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 비밀 이름의 비밀의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="9ea70-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="9ea70-133">-OutputFile</span></span>
<span data-ttu-id="9ea70-134">출력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-134">Output file.</span></span>
<span data-ttu-id="9ea70-135">인증서의 백업을 저장할 출력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="9ea70-136">지정하지 않으면 기본 파일 이름이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-136">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="9ea70-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9ea70-137">-VaultName</span></span>
<span data-ttu-id="9ea70-138">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-138">Vault name.</span></span>
<span data-ttu-id="9ea70-139">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="9ea70-140">-확인</span><span class="sxs-lookup"><span data-stu-id="9ea70-140">-Confirm</span></span>
<span data-ttu-id="9ea70-141">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ea70-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ea70-142">-WhatIf</span></span>
<span data-ttu-id="9ea70-143">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ea70-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ea70-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ea70-145">CommonParameters</span></span>
<span data-ttu-id="9ea70-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea70-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ea70-147">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ea70-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ea70-148">입력</span><span class="sxs-lookup"><span data-stu-id="9ea70-148">INPUTS</span></span>

### <span data-ttu-id="9ea70-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9ea70-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="9ea70-150">출력</span><span class="sxs-lookup"><span data-stu-id="9ea70-150">OUTPUTS</span></span>

### <span data-ttu-id="9ea70-151">System.String</span><span class="sxs-lookup"><span data-stu-id="9ea70-151">System.String</span></span>

## <span data-ttu-id="9ea70-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9ea70-152">NOTES</span></span>

## <span data-ttu-id="9ea70-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ea70-153">RELATED LINKS</span></span>
