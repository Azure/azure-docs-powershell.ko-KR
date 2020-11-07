---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultCertificate.md
ms.openlocfilehash: 7955ecd02d40ac3dff891b8eb315a39ccf985ebb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711370"
---
# <span data-ttu-id="ffcad-101">Restore-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ffcad-101">Restore-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="ffcad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffcad-102">SYNOPSIS</span></span>
<span data-ttu-id="ffcad-103">백업 파일에서 키 보관소의 인증서를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcad-103">Restores a certificate in a key vault from a backup file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffcad-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ffcad-104">SYNTAX</span></span>

### <span data-ttu-id="ffcad-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="ffcad-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultCertificate [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffcad-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ffcad-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffcad-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ffcad-107">ByResourceId</span></span>
```
Restore-AzureKeyVaultCertificate [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffcad-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ffcad-108">DESCRIPTION</span></span>
<span data-ttu-id="ffcad-109">**Restore-AzureKeyVaultCertificate** cmdlet은 백업 파일에서 지정 된 키 보관소에 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ffcad-109">The **Restore-AzureKeyVaultCertificate** cmdlet creates a certificate in the specified key vault from a backup file.</span></span>
<span data-ttu-id="ffcad-110">이 인증서는 입력 파일에 있는 백업 된 인증서의 복제본 이며 원래 인증서와 같은 이름을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="ffcad-110">This certificate is a replica of the backed-up certificate in the input file and has the same name as the original certificate.</span></span>
<span data-ttu-id="ffcad-111">키 자격 증명 모음에 같은 이름의 인증서가 이미 포함 되어 있는 경우에는 원래 인증서를 덮어쓰지 않고이 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcad-111">If the key vault already contains a certificate by the same name, this cmdlet fails instead of overwriting the original certificate.</span></span>
<span data-ttu-id="ffcad-112">백업에 여러 버전의 인증서가 포함 되어 있으면 모든 버전이 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffcad-112">If the backup contains multiple versions of a certificate, all versions are restored.</span></span>
<span data-ttu-id="ffcad-113">인증서를 복원 하는 키 보관소는 인증서를 백업한 키 보관소와 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffcad-113">The key vault that you restore the certificate into can be different from the key vault that you backed up the certificate from.</span></span>
<span data-ttu-id="ffcad-114">그러나 키 자격 증명 모음이 동일한 구독을 사용 해야 하며 같은 지리 (예: 북미)의 Azure 지역에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcad-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="ffcad-115"> https://azure.microsoft.com/support/trust-center/)Azure 지역을 지역에 매핑하는 Microsoft Azure 보안 센터를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ffcad-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="ffcad-116">예제의</span><span class="sxs-lookup"><span data-stu-id="ffcad-116">EXAMPLES</span></span>

### <span data-ttu-id="ffcad-117">예제 1: 백업 된 인증서 복원</span><span class="sxs-lookup"><span data-stu-id="ffcad-117">Example 1: Restore a backed-up certificate</span></span>
```powershell
PS C:\> Restore-AzureKeyVaultCertificate -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/25/2018 3:47:41 AM

                [Not After]
                  11/25/2018 2:57:41 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Purgeable
Enabled       : True
Expires       : 11/25/2018 10:57:41 AM
NotBefore     : 5/25/2018 10:47:41 AM
Created       : 5/25/2018 10:57:41 AM
Updated       : 5/25/2018 10:57:41 AM
Tags          : 
VaultName     : MyKeyVault
Name          : cert1
Version       : bd406f6d6b3a41a1a1c633494d8c3c3a
Id            : https://mykeyvault.vault.azure.net:443/certificates/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
```

<span data-ttu-id="ffcad-118">이 명령은 백업 파일의 모든 버전을 포함 하는 인증서를 MyKeyVault 이라는 키 자격 증명 모음으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcad-118">This command restores a certificate, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="ffcad-119">변수</span><span class="sxs-lookup"><span data-stu-id="ffcad-119">PARAMETERS</span></span>

### <span data-ttu-id="ffcad-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffcad-120">-DefaultProfile</span></span>
<span data-ttu-id="ffcad-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ffcad-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffcad-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="ffcad-122">-InputFile</span></span>
<span data-ttu-id="ffcad-123">입력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="ffcad-123">Input file.</span></span>
<span data-ttu-id="ffcad-124">백업 된 blob을 포함 하는 입력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="ffcad-124">The input file containing the backed-up blob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcad-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffcad-125">-InputObject</span></span>
<span data-ttu-id="ffcad-126">KeyVault 개체</span><span class="sxs-lookup"><span data-stu-id="ffcad-126">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffcad-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ffcad-127">-ResourceId</span></span>
<span data-ttu-id="ffcad-128">KeyVault 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="ffcad-128">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffcad-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ffcad-129">-VaultName</span></span>
<span data-ttu-id="ffcad-130">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="ffcad-130">Vault name.</span></span>
<span data-ttu-id="ffcad-131">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcad-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcad-132">-확인</span><span class="sxs-lookup"><span data-stu-id="ffcad-132">-Confirm</span></span>
<span data-ttu-id="ffcad-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcad-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffcad-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffcad-134">-WhatIf</span></span>
<span data-ttu-id="ffcad-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ffcad-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffcad-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffcad-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffcad-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffcad-137">CommonParameters</span></span>
<span data-ttu-id="ffcad-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcad-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffcad-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffcad-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffcad-140">입력</span><span class="sxs-lookup"><span data-stu-id="ffcad-140">INPUTS</span></span>

### <span data-ttu-id="ffcad-141">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ffcad-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="ffcad-142">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ffcad-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ffcad-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ffcad-143">System.String</span></span>

## <span data-ttu-id="ffcad-144">출력</span><span class="sxs-lookup"><span data-stu-id="ffcad-144">OUTPUTS</span></span>

### <span data-ttu-id="ffcad-145">Microsoft. KeyVault. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ffcad-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="ffcad-146">상속자</span><span class="sxs-lookup"><span data-stu-id="ffcad-146">NOTES</span></span>

## <span data-ttu-id="ffcad-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ffcad-147">RELATED LINKS</span></span>
