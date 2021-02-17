---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: c3ddf8373b467b3f7821d9470f67f2b864201949
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178577"
---
# <span data-ttu-id="696bf-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="696bf-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="696bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="696bf-102">SYNOPSIS</span></span>
<span data-ttu-id="696bf-103">클러스터에 보조 클러스터 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="696bf-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="696bf-104">구문</span><span class="sxs-lookup"><span data-stu-id="696bf-104">SYNTAX</span></span>

### <span data-ttu-id="696bf-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="696bf-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-Thumbprint <String>] [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="696bf-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="696bf-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="696bf-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="696bf-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="696bf-108">설명</span><span class="sxs-lookup"><span data-stu-id="696bf-108">DESCRIPTION</span></span>
<span data-ttu-id="696bf-109">**Add-AzServiceFabricClusterCertificate를** 사용하여 기존 Azure Key Vault에서 보조 클러스터 인증서를 추가하거나 제공된 기존 인증서를 사용하여 새 Azure Key Vault를 만들거나 새로 만든 자체 서명된 인증서에서 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="696bf-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="696bf-110">보조 클러스터가 있는 경우 보조 클러스터를 다시 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="696bf-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="696bf-111">예제</span><span class="sxs-lookup"><span data-stu-id="696bf-111">EXAMPLES</span></span>

### <span data-ttu-id="696bf-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="696bf-112">Example 1</span></span>
```powershell
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="696bf-113">이 명령은 기존 Azure Key Vault에 인증서를 보조 클러스터 인증서로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="696bf-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="696bf-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="696bf-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="696bf-115">이 명령은 Azure Key Vault에 자체 서명된 인증서를 만들고 클러스터를 업그레이드하여 보조 클러스터 인증서로 사용하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="696bf-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="696bf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="696bf-116">PARAMETERS</span></span>

### <span data-ttu-id="696bf-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="696bf-117">-CertificateCommonName</span></span>
<span data-ttu-id="696bf-118">인증서 일반 이름</span><span class="sxs-lookup"><span data-stu-id="696bf-118">Certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertCommonName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696bf-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="696bf-119">-CertificateFile</span></span>
<span data-ttu-id="696bf-120">기존 인증서의 경로</span><span class="sxs-lookup"><span data-stu-id="696bf-120">The path to the existing certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: Source

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="696bf-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="696bf-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="696bf-122">인증서 발급자 지문( 두 개 이상인 경우 콤마로 구분)</span><span class="sxs-lookup"><span data-stu-id="696bf-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertIssuerThumbprint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696bf-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="696bf-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="696bf-124">새 인증서를 다운로드해야 하는 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="696bf-124">The folder where the new certificate needs to be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="696bf-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="696bf-125">-CertificatePassword</span></span>
<span data-ttu-id="696bf-126">인증서의 암호</span><span class="sxs-lookup"><span data-stu-id="696bf-126">The password of the certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="696bf-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="696bf-127">-CertificateSubjectName</span></span>
<span data-ttu-id="696bf-128">인증서의 주체 이름</span><span class="sxs-lookup"><span data-stu-id="696bf-128">The subject name of the certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Subject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="696bf-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="696bf-129">-DefaultProfile</span></span>
<span data-ttu-id="696bf-130">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="696bf-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="696bf-131">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="696bf-131">-KeyVaultName</span></span>
<span data-ttu-id="696bf-132">Azure Key Vault 이름이 지정되지 않은 경우 리소스 그룹 이름으로 기본값이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="696bf-132">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="696bf-133">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="696bf-133">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="696bf-134">Azure Key Vault 리소스 그룹 이름이 지정되지 않은 경우 리소스 그룹 이름으로 기본값이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="696bf-134">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: KeyVaultResouceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="696bf-135">-Name</span><span class="sxs-lookup"><span data-stu-id="696bf-135">-Name</span></span>
<span data-ttu-id="696bf-136">클러스터의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="696bf-136">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696bf-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="696bf-137">-ResourceGroupName</span></span>
<span data-ttu-id="696bf-138">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="696bf-138">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="696bf-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="696bf-139">-SecretIdentifier</span></span>
<span data-ttu-id="696bf-140">기존 Azure Key Vault 비밀 URL(예: https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f ''</span><span class="sxs-lookup"><span data-stu-id="696bf-140">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="696bf-141">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="696bf-141">-Thumbprint</span></span>
<span data-ttu-id="696bf-142">SecretIdentifier에 대한 인증서 correspoinding에 대한 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="696bf-142">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="696bf-143">키 자격 증명 모음에 인증서만 비밀로 저장되고 cmdlet이 지문을 검색할 수 없는 경우 인증서가 관리되지 않는 경우 이 방법을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="696bf-143">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="696bf-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="696bf-144">-Confirm</span></span>
<span data-ttu-id="696bf-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="696bf-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="696bf-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="696bf-146">-WhatIf</span></span>
<span data-ttu-id="696bf-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="696bf-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="696bf-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="696bf-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="696bf-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="696bf-149">CommonParameters</span></span>
<span data-ttu-id="696bf-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="696bf-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="696bf-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="696bf-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="696bf-152">입력</span><span class="sxs-lookup"><span data-stu-id="696bf-152">INPUTS</span></span>

### <span data-ttu-id="696bf-153">System.String</span><span class="sxs-lookup"><span data-stu-id="696bf-153">System.String</span></span>

### <span data-ttu-id="696bf-154">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="696bf-154">System.Security.SecureString</span></span>

## <span data-ttu-id="696bf-155">출력</span><span class="sxs-lookup"><span data-stu-id="696bf-155">OUTPUTS</span></span>

### <span data-ttu-id="696bf-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="696bf-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="696bf-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="696bf-157">NOTES</span></span>

## <span data-ttu-id="696bf-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="696bf-158">RELATED LINKS</span></span>

[<span data-ttu-id="696bf-159">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="696bf-159">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="696bf-160">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="696bf-160">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
