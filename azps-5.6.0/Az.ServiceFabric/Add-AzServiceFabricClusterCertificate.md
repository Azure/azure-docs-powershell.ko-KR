---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 379bd710413fee83a2fdb6b10dc7fb42f0f207bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969872"
---
# <span data-ttu-id="f8847-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f8847-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="f8847-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8847-102">SYNOPSIS</span></span>
<span data-ttu-id="f8847-103">클러스터에 보조 클러스터 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f8847-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="f8847-104">구문</span><span class="sxs-lookup"><span data-stu-id="f8847-104">SYNTAX</span></span>

### <span data-ttu-id="f8847-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="f8847-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-Thumbprint <String>] [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8847-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="f8847-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8847-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="f8847-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8847-108">설명</span><span class="sxs-lookup"><span data-stu-id="f8847-108">DESCRIPTION</span></span>
<span data-ttu-id="f8847-109">**Add-AzServiceFabricClusterCertificate를** 사용하여 기존 Azure 키 자격 증명 모음에서 보조 클러스터 인증서를 추가하거나 제공된 기존 인증서를 사용하여 새 Azure 키 자격 증명 모음을 만들거나 만든 새 자체 서명된 인증서에서 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8847-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="f8847-110">있는 경우 보조 클러스터를 다시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8847-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="f8847-111">예제</span><span class="sxs-lookup"><span data-stu-id="f8847-111">EXAMPLES</span></span>

### <span data-ttu-id="f8847-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="f8847-112">Example 1</span></span>
```powershell
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="f8847-113">이 명령은 기존 Azure 키 자격 증명 모음에 보조 클러스터 인증서로 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f8847-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="f8847-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="f8847-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="f8847-115">이 명령은 Azure 키 자격 증명 모음에서 자체 서명된 인증서를 만들고 클러스터를 업그레이드하여 보조 클러스터 인증서로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8847-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="f8847-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f8847-116">PARAMETERS</span></span>

### <span data-ttu-id="f8847-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="f8847-117">-CertificateCommonName</span></span>
<span data-ttu-id="f8847-118">인증서 일반 이름</span><span class="sxs-lookup"><span data-stu-id="f8847-118">Certificate common name</span></span>

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

### <span data-ttu-id="f8847-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f8847-119">-CertificateFile</span></span>
<span data-ttu-id="f8847-120">기존 인증서에 대한 경로</span><span class="sxs-lookup"><span data-stu-id="f8847-120">The path to the existing certificate</span></span>

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

### <span data-ttu-id="f8847-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="f8847-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="f8847-122">인증서 발급자 지문(하나 이상의 경우 콤마로 구분)</span><span class="sxs-lookup"><span data-stu-id="f8847-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="f8847-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="f8847-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="f8847-124">새 인증서를 다운로드해야 하는 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="f8847-124">The folder where the new certificate needs to be downloaded.</span></span>

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

### <span data-ttu-id="f8847-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="f8847-125">-CertificatePassword</span></span>
<span data-ttu-id="f8847-126">인증서의 암호</span><span class="sxs-lookup"><span data-stu-id="f8847-126">The password of the certificate</span></span>

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

### <span data-ttu-id="f8847-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="f8847-127">-CertificateSubjectName</span></span>
<span data-ttu-id="f8847-128">인증서의 제목 이름</span><span class="sxs-lookup"><span data-stu-id="f8847-128">The subject name of the certificate</span></span>

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

### <span data-ttu-id="f8847-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8847-129">-DefaultProfile</span></span>
<span data-ttu-id="f8847-130">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f8847-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8847-131">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="f8847-131">-KeyVaultName</span></span>
<span data-ttu-id="f8847-132">Azure 키 자격 증명 모음 이름(지정되지 않은 경우 리소스 그룹 이름에 기본값이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8847-132">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="f8847-133">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8847-133">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="f8847-134">Azure 키 자격 증명 모음 리소스 그룹 이름(지정되지 않은 경우 리소스 그룹 이름)은 기본값으로 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8847-134">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="f8847-135">-Name</span><span class="sxs-lookup"><span data-stu-id="f8847-135">-Name</span></span>
<span data-ttu-id="f8847-136">클러스터의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="f8847-136">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="f8847-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8847-137">-ResourceGroupName</span></span>
<span data-ttu-id="f8847-138">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8847-138">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="f8847-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="f8847-139">-SecretIdentifier</span></span>
<span data-ttu-id="f8847-140">기존 Azure 키 자격 증명 모음 비밀 URL(예: https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f ''</span><span class="sxs-lookup"><span data-stu-id="f8847-140">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="f8847-141">-지문</span><span class="sxs-lookup"><span data-stu-id="f8847-141">-Thumbprint</span></span>
<span data-ttu-id="f8847-142">SecretIdentifier에 대한 인증서 correspoinding에 대한 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="f8847-142">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="f8847-143">인증서가 키 자격 증명 모음에 비밀로만 저장되고 cmdlet이 지문을 복구할 수 없는 경우 이 방법을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8847-143">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

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

### <span data-ttu-id="f8847-144">-확인</span><span class="sxs-lookup"><span data-stu-id="f8847-144">-Confirm</span></span>
<span data-ttu-id="f8847-145">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8847-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8847-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8847-146">-WhatIf</span></span>
<span data-ttu-id="f8847-147">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f8847-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8847-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8847-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8847-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8847-149">CommonParameters</span></span>
<span data-ttu-id="f8847-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f8847-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8847-151">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8847-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8847-152">입력</span><span class="sxs-lookup"><span data-stu-id="f8847-152">INPUTS</span></span>

### <span data-ttu-id="f8847-153">System.String</span><span class="sxs-lookup"><span data-stu-id="f8847-153">System.String</span></span>

### <span data-ttu-id="f8847-154">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="f8847-154">System.Security.SecureString</span></span>

## <span data-ttu-id="f8847-155">출력</span><span class="sxs-lookup"><span data-stu-id="f8847-155">OUTPUTS</span></span>

### <span data-ttu-id="f8847-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="f8847-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="f8847-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f8847-157">NOTES</span></span>

## <span data-ttu-id="f8847-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8847-158">RELATED LINKS</span></span>

[<span data-ttu-id="f8847-159">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f8847-159">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="f8847-160">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="f8847-160">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
