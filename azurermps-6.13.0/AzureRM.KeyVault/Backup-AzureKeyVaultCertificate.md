---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
ms.openlocfilehash: 7f75f07ee8f53a57cdb2e359fb4addb51b1d7f76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527936"
---
# <span data-ttu-id="70ded-101">Backup-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="70ded-101">Backup-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="70ded-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70ded-102">SYNOPSIS</span></span>
<span data-ttu-id="70ded-103">키 자격 증명 모음에서 인증서를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-103">Backs up a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70ded-104">구문과</span><span class="sxs-lookup"><span data-stu-id="70ded-104">SYNTAX</span></span>

### <span data-ttu-id="70ded-105">ByCertificateName (기본값)</span><span class="sxs-lookup"><span data-stu-id="70ded-105">ByCertificateName (Default)</span></span>
```
Backup-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70ded-106">ByCertificate</span><span class="sxs-lookup"><span data-stu-id="70ded-106">ByCertificate</span></span>
```
Backup-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70ded-107">설명은</span><span class="sxs-lookup"><span data-stu-id="70ded-107">DESCRIPTION</span></span>
<span data-ttu-id="70ded-108">**AzureKeyVaultCertificate** cmdlet은 지정 된 인증서를 다운로드 하 고 파일에 저장 하 여 키 보관소에 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-108">The **Backup-AzureKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="70ded-109">인증서에 여러 버전이 있으면 모든 버전이 백업에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="70ded-110">다운로드 된 콘텐츠는 암호화 되어 있으므로 Azure 키 자격 증명 모음 외부에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="70ded-111">인증서가 백업 된 구독의 모든 키 보관소 (자격 증명 모음이 동일한 Azure 지리에 있는 경우)로 복구 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="70ded-112">이 cmdlet을 사용 하는 일반적인 이유는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="70ded-113">자격 증명 모음에서 원본을 실수로 삭제 한 경우에 대비 하 여 인증서의 오프 라인 복사본을 유지 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="70ded-114">키 자격 증명 모음을 사용 하 여 인증서를 만든 후 분산 응용 프로그램의 모든 인스턴스에서 사용할 수 있도록 개체를 다른 Azure 지역에 복제 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="70ded-115">**AzureKeyVaultCertificate** cmdlet을 사용 하 여 암호화 된 형식으로 인증서를 검색 한 다음 **Restore-AzureKeyVaultCertificate** cmdlet을 사용 하 고 두 번째 지역에서 키 자격 증명 모음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-115">Use the **Backup-AzureKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzureKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="70ded-116">예제의</span><span class="sxs-lookup"><span data-stu-id="70ded-116">EXAMPLES</span></span>

### <span data-ttu-id="70ded-117">예제 1: 자동으로 생성 된 파일 이름으로 인증서 백업</span><span class="sxs-lookup"><span data-stu-id="70ded-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="70ded-118">이 명령은 MyKeyVault 이라는 키 자격 증명 모음에서 MyCert 이라는 인증서를 검색 하 고, 해당 인증서의 백업을 자동으로 이름이 지정 된 파일에 저장 하 고, 파일 이름을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="70ded-119">예제 2: 인증서를 지정 된 파일 이름으로 백업</span><span class="sxs-lookup"><span data-stu-id="70ded-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="70ded-120">이 명령은 MyKeyVault 이라는 키 자격 증명 모음에서 MyCert 이라는 인증서를 검색 하 고 해당 인증서의 백업을 blob 라는 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="70ded-121">예제 3: 이전에 검색 한 인증서를 지정 된 파일 이름으로 백업 하 고 메시지를 표시 하지 않고 대상 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzureKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzureKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="70ded-122">이 명령은 $cert 라는 인증서의 백업을 만듭니다. $Cert의 자격 증명 모음에 이름으로 지정 합니다. VaultName 파일에 이미 있는 경우 파일을 자동으로 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="70ded-123">변수</span><span class="sxs-lookup"><span data-stu-id="70ded-123">PARAMETERS</span></span>

### <span data-ttu-id="70ded-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70ded-124">-DefaultProfile</span></span>
<span data-ttu-id="70ded-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70ded-126">-Force</span><span class="sxs-lookup"><span data-stu-id="70ded-126">-Force</span></span>
<span data-ttu-id="70ded-127">지정 된 파일 (있는 경우)을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="70ded-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70ded-128">-InputObject</span></span>
<span data-ttu-id="70ded-129">백업할 비밀을 검색 호출의 출력에서 파이프라인으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="70ded-130">-이름</span><span class="sxs-lookup"><span data-stu-id="70ded-130">-Name</span></span>
<span data-ttu-id="70ded-131">비밀 이름.</span><span class="sxs-lookup"><span data-stu-id="70ded-131">Secret name.</span></span>
<span data-ttu-id="70ded-132">Cmdlet은 자격 증명 정보, 현재 선택 된 환경 및 비밀 이름 으로부터 비밀의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="70ded-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="70ded-133">-OutputFile</span></span>
<span data-ttu-id="70ded-134">출력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-134">Output file.</span></span>
<span data-ttu-id="70ded-135">인증서 백업을 저장할 출력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="70ded-136">지정 하지 않으면 기본 파일 이름이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-136">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="70ded-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="70ded-137">-VaultName</span></span>
<span data-ttu-id="70ded-138">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="70ded-138">Vault name.</span></span>
<span data-ttu-id="70ded-139">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="70ded-140">-확인</span><span class="sxs-lookup"><span data-stu-id="70ded-140">-Confirm</span></span>
<span data-ttu-id="70ded-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70ded-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70ded-142">-WhatIf</span></span>
<span data-ttu-id="70ded-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70ded-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70ded-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70ded-145">CommonParameters</span></span>
<span data-ttu-id="70ded-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="70ded-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70ded-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70ded-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70ded-148">입력</span><span class="sxs-lookup"><span data-stu-id="70ded-148">INPUTS</span></span>

### <span data-ttu-id="70ded-149">Microsoft. KeyVault. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="70ded-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="70ded-150">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="70ded-150">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="70ded-151">출력</span><span class="sxs-lookup"><span data-stu-id="70ded-151">OUTPUTS</span></span>

### <span data-ttu-id="70ded-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="70ded-152">System.String</span></span>

## <span data-ttu-id="70ded-153">상속자</span><span class="sxs-lookup"><span data-stu-id="70ded-153">NOTES</span></span>

## <span data-ttu-id="70ded-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70ded-154">RELATED LINKS</span></span>
