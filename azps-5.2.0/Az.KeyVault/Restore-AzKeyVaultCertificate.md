---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
ms.openlocfilehash: 298d6bac6b2c1b37cff47a22a1647caafdb3e843
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354926"
---
# <span data-ttu-id="86c15-101">Restore-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="86c15-101">Restore-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="86c15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86c15-102">SYNOPSIS</span></span>
<span data-ttu-id="86c15-103">백업 파일에서 키 자격 증명 모음의 인증서를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="86c15-103">Restores a certificate in a key vault from a backup file.</span></span>

## <span data-ttu-id="86c15-104">구문</span><span class="sxs-lookup"><span data-stu-id="86c15-104">SYNTAX</span></span>

### <span data-ttu-id="86c15-105">ByVaultName(기본값)</span><span class="sxs-lookup"><span data-stu-id="86c15-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultCertificate [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86c15-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="86c15-106">ByInputObject</span></span>
```
Restore-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86c15-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="86c15-107">ByResourceId</span></span>
```
Restore-AzKeyVaultCertificate [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86c15-108">설명</span><span class="sxs-lookup"><span data-stu-id="86c15-108">DESCRIPTION</span></span>
<span data-ttu-id="86c15-109">**Restore-AzKeyVaultCertificate** cmdlet은 백업 파일에서 지정된 키 자격 증명 모음에 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="86c15-109">The **Restore-AzKeyVaultCertificate** cmdlet creates a certificate in the specified key vault from a backup file.</span></span>
<span data-ttu-id="86c15-110">이 인증서는 입력 파일의 백업된 인증서 복제본으로, 원래 인증서와 이름이 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="86c15-110">This certificate is a replica of the backed-up certificate in the input file and has the same name as the original certificate.</span></span>
<span data-ttu-id="86c15-111">Key Vault에 동일한 이름의 인증서가 이미 포함되어 있는 경우 이 cmdlet은 원래 인증서를 덮어써야 하는 대신 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="86c15-111">If the key vault already contains a certificate by the same name, this cmdlet fails instead of overwriting the original certificate.</span></span>
<span data-ttu-id="86c15-112">백업에 여러 버전의 인증서가 포함되어 있는 경우 모든 버전이 복원됩니다.</span><span class="sxs-lookup"><span data-stu-id="86c15-112">If the backup contains multiple versions of a certificate, all versions are restored.</span></span>
<span data-ttu-id="86c15-113">인증서를 복원하는 키 자격 증명 모음은 인증서를 백업한 키 자격 증명 모음과 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86c15-113">The key vault that you restore the certificate into can be different from the key vault that you backed up the certificate from.</span></span>
<span data-ttu-id="86c15-114">그러나 Key Vault는 동일한 구독을 사용하며 동일한 지역(예: 북아메리카)의 Azure 지역에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="86c15-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="86c15-115">Azure 지역을 지역에 매핑하는 경우 Microsoft Azure 보안 센터를 https://azure.microsoft.com/support/trust-center/) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="86c15-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="86c15-116">예제</span><span class="sxs-lookup"><span data-stu-id="86c15-116">EXAMPLES</span></span>

### <span data-ttu-id="86c15-117">예제 1: 백업된 인증서 복원</span><span class="sxs-lookup"><span data-stu-id="86c15-117">Example 1: Restore a backed-up certificate</span></span>
```powershell
PS C:\> Restore-AzKeyVaultCertificate -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

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

<span data-ttu-id="86c15-118">이 명령은 Backup.blob이라는 백업 파일에서 MyKeyVault라는 키 자격 증명 모음으로 모든 버전을 포함한 인증서를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="86c15-118">This command restores a certificate, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="86c15-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86c15-119">PARAMETERS</span></span>

### <span data-ttu-id="86c15-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86c15-120">-DefaultProfile</span></span>
<span data-ttu-id="86c15-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="86c15-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86c15-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="86c15-122">-InputFile</span></span>
<span data-ttu-id="86c15-123">입력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="86c15-123">Input file.</span></span>
<span data-ttu-id="86c15-124">백업된 Blob을 포함하는 입력 파일</span><span class="sxs-lookup"><span data-stu-id="86c15-124">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="86c15-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86c15-125">-InputObject</span></span>
<span data-ttu-id="86c15-126">KeyVault 개체</span><span class="sxs-lookup"><span data-stu-id="86c15-126">KeyVault object</span></span>

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

### <span data-ttu-id="86c15-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86c15-127">-ResourceId</span></span>
<span data-ttu-id="86c15-128">KeyVault 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="86c15-128">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="86c15-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="86c15-129">-VaultName</span></span>
<span data-ttu-id="86c15-130">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86c15-130">Vault name.</span></span>
<span data-ttu-id="86c15-131">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="86c15-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="86c15-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86c15-132">-Confirm</span></span>
<span data-ttu-id="86c15-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="86c15-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86c15-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86c15-134">-WhatIf</span></span>
<span data-ttu-id="86c15-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="86c15-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86c15-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86c15-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86c15-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c15-137">CommonParameters</span></span>
<span data-ttu-id="86c15-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="86c15-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c15-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="86c15-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c15-140">입력</span><span class="sxs-lookup"><span data-stu-id="86c15-140">INPUTS</span></span>

### <span data-ttu-id="86c15-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="86c15-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="86c15-142">System.String</span><span class="sxs-lookup"><span data-stu-id="86c15-142">System.String</span></span>

## <span data-ttu-id="86c15-143">출력</span><span class="sxs-lookup"><span data-stu-id="86c15-143">OUTPUTS</span></span>

### <span data-ttu-id="86c15-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="86c15-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="86c15-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="86c15-145">NOTES</span></span>

## <span data-ttu-id="86c15-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86c15-146">RELATED LINKS</span></span>
