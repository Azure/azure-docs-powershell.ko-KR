---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
ms.openlocfilehash: 9e5ba2d2ee228da30a887c0c7b318dd9d270d763
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208021"
---
# <span data-ttu-id="90e25-101">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="90e25-101">New-AzServiceFabricCluster</span></span>

## <span data-ttu-id="90e25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90e25-102">SYNOPSIS</span></span>

<span data-ttu-id="90e25-103">이 명령은 사용자가 제공하는 인증서를 사용하거나 시스템에서 자체 서명된 인증서를 생성하여 새 Service Fabric 클러스터를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="90e25-104">기본 템플릿 또는 사용자가 제공하는 사용자 지정 템플릿을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="90e25-105">자체 서명된 인증서를 내보낼 폴더를 지정하거나 나중에 키 자격 증명 모음에서 해당 인증서를 인출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

## <span data-ttu-id="90e25-106">구문</span><span class="sxs-lookup"><span data-stu-id="90e25-106">SYNTAX</span></span>

### <span data-ttu-id="90e25-107">ByDefaultArmTemplate(기본값)</span><span class="sxs-lookup"><span data-stu-id="90e25-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90e25-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="90e25-108">ByExistingKeyVault</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 -SecretIdentifier <String> [-Thumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90e25-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="90e25-109">ByNewPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>]
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateSubjectName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90e25-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="90e25-110">ByExistingPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90e25-111">설명</span><span class="sxs-lookup"><span data-stu-id="90e25-111">DESCRIPTION</span></span>

<span data-ttu-id="90e25-112">**New-AzServiceFabricCluster** 명령은 사용자가 제공하거나 시스템에서 자체 서명된 인증서를 생성한 인증서를 사용하여 새 Service Fabric 클러스터를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-112">The **New-AzServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="90e25-113">사용되는 템플릿은 기본 템플릿 또는 사용자가 제공하는 사용자 지정 템플릿일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="90e25-114">자체 서명된 인증서를 내보낼 폴더를 지정하거나 나중에 키 자격 증명 모음에서 해당 인증서를 인출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="90e25-115">사용자 지정 템플릿 및 매개 변수 파일을 지정하는 경우 매개 변수 파일에 인증서 정보를 제공할 필요가 없습니다. 시스템에서 이러한 매개 변수를 채우게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="90e25-116">네 가지 옵션은 아래에 자세히 설명됩니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-116">The four options are detailed below.</span></span> <span data-ttu-id="90e25-117">각 매개 변수에 대한 설명을 위해 아래로 스크롤합니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="90e25-118">예제</span><span class="sxs-lookup"><span data-stu-id="90e25-118">EXAMPLES</span></span>

### <span data-ttu-id="90e25-119">예제 1: 클러스터를 배포할 클러스터 크기, 인증 주체 이름 및 OS만 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -f $resourceGroupName, $azureRegion
$localCertificateFolder = "c:\certs"

Write-Output "Create cluster in '$azureRegion' with cert subject name '$clusterDnsName' and cert output path '$localCertificateFolder'"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -Location $azureRegion -ClusterSize 5 -VmPassword $password -CertificateSubjectName $clusterDnsName -CertificateOutputFolder $localCertificateFolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="90e25-120">이 명령은 클러스터를 배포할 클러스터 크기, 인증 주체 이름 및 OS만 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="90e25-121">예제 2: 키 자격 증명 모음의 기존 인증서 리소스 및 클러스터를 배포할 사용자 지정 템플릿 지정</span><span class="sxs-lookup"><span data-stu-id="90e25-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>

```powershell
$resourceGroupName = "test20"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId = "https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -SecretIdentifier $secretId
```

<span data-ttu-id="90e25-122">이 명령은 키 자격 증명 모음의 기존 인증서 리소스와 클러스터를 배포할 사용자 지정 템플릿을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="90e25-123">예제 3: 사용자 지정 템플릿을 사용하여 새 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="90e25-124">키 자격 증명 모음에 다른 리소스 그룹 이름을 지정하고 시스템에 새 인증서를 업로드하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$keyVaultResourceGroupName = " quickstart-kv-group"
$keyVaultName = "quickstart-kv"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -F $resourceGroupName, $azureRegion
$localCertificateFolder = "~\Documents"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -CertificateOutputFolder $localCertificateFolder -CertificatePassword $password -KeyVaultResourceGroupName $keyVaultResourceGroupName  -KeyVaultName $keyVaultName -CertificateSubjectName $clusterDnsName
```

<span data-ttu-id="90e25-125">이 명령은 사용자 지정 템플릿을 사용하여 새 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="90e25-126">키 자격 증명 모음에 다른 리소스 그룹 이름을 지정하고 시스템에 새 인증서를 업로드하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="90e25-127">예제 4: 사용자 지정 인증서 및 사용자 지정 템플릿 가져오기 및 새 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="90e25-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "test20"
$keyVaultResourceGroupName = "test20kvrg"
$keyVaultName = "test20kv"
$localCertificateFile = "c:\Mycertificates\my2017Prodcert.pfx"
$templateParameterFile = "~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -CertificateFile $localCertificateFile -CertificatePassword $password -KeyVaultResourceGroupName $keyVaultResourceGroupName -KeyVaultName $keyVaultName
```

<span data-ttu-id="90e25-128">이 명령을 사용하면 사용자 지정 인증서 및 사용자 지정 템플릿을 가져오고 새 클러스터를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="90e25-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90e25-129">PARAMETERS</span></span>

### <span data-ttu-id="90e25-130">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="90e25-130">-CertificateCommonName</span></span>

<span data-ttu-id="90e25-131">인증서 일반 이름</span><span class="sxs-lookup"><span data-stu-id="90e25-131">Certificate common name</span></span>

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

### <span data-ttu-id="90e25-132">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="90e25-132">-CertificateFile</span></span>

<span data-ttu-id="90e25-133">기본 클러스터 인증서에 대한 기존 인증서 파일 경로</span><span class="sxs-lookup"><span data-stu-id="90e25-133">The existing certificate file path for the primary cluster certificate</span></span>

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

### <span data-ttu-id="90e25-134">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="90e25-134">-CertificateIssuerThumbprint</span></span>

<span data-ttu-id="90e25-135">인증서 발급자 지문( 두 개 이상인 경우 콤마로 구분)</span><span class="sxs-lookup"><span data-stu-id="90e25-135">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="90e25-136">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="90e25-136">-CertificateOutputFolder</span></span>

<span data-ttu-id="90e25-137">만들 새 인증서 파일의 폴더</span><span class="sxs-lookup"><span data-stu-id="90e25-137">The folder of the new certificate file to be created</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e25-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="90e25-138">-CertificatePassword</span></span>

<span data-ttu-id="90e25-139">인증서 파일의 암호</span><span class="sxs-lookup"><span data-stu-id="90e25-139">The password of the certificate file</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e25-140">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="90e25-140">-CertificateSubjectName</span></span>

<span data-ttu-id="90e25-141">만들 인증서의 주체 이름</span><span class="sxs-lookup"><span data-stu-id="90e25-141">The subject name of the certificate to be created</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Subject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e25-142">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="90e25-142">-ClusterSize</span></span>

<span data-ttu-id="90e25-143">클러스터의 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-143">The number of nodes in the cluster.</span></span>
<span data-ttu-id="90e25-144">기본값은 5개 노드입니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-144">Default are 5 nodes</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e25-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e25-145">-DefaultProfile</span></span>

<span data-ttu-id="90e25-146">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90e25-147">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="90e25-147">-KeyVaultName</span></span>

<span data-ttu-id="90e25-148">Azure Key Vault 이름이 지정되지 않은 경우 리소스 그룹 이름으로 기본값이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-148">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e25-149">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90e25-149">-KeyVaultResourceGroupName</span></span>

<span data-ttu-id="90e25-150">Azure Key Vault 리소스 그룹 이름이 지정되지 않은 경우 리소스 그룹 이름으로 기본값이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-150">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: KeyVaultResouceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e25-151">-Location</span><span class="sxs-lookup"><span data-stu-id="90e25-151">-Location</span></span>

<span data-ttu-id="90e25-152">리소스 그룹 위치</span><span class="sxs-lookup"><span data-stu-id="90e25-152">The resource group location</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e25-153">-Name</span><span class="sxs-lookup"><span data-stu-id="90e25-153">-Name</span></span>

<span data-ttu-id="90e25-154">클러스터의 이름을 지정합니다. 지정하지 않으면 리소스 그룹 이름과 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-154">Specify the name of the cluster, if not given it will be same as resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: ClusterName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e25-155">-OS</span><span class="sxs-lookup"><span data-stu-id="90e25-155">-OS</span></span>

<span data-ttu-id="90e25-156">클러스터를 구성하는 VM의 운영 체제입니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-156">The Operating System of the VMs that make up the cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem
Parameter Sets: ByDefaultArmTemplate
Aliases: VmImage
Accepted values: WindowsServer2012R2Datacenter, WindowsServer2016Datacenter, WindowsServer2016DatacenterwithContainers, UbuntuServer1604

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e25-157">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="90e25-157">-ParameterFile</span></span>

<span data-ttu-id="90e25-158">템플릿 매개 변수 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-158">The path to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e25-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90e25-159">-ResourceGroupName</span></span>

<span data-ttu-id="90e25-160">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-160">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="90e25-161">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="90e25-161">-SecondaryCertificateFile</span></span>

<span data-ttu-id="90e25-162">보조 클러스터 인증서에 대한 기존 인증서 파일 경로</span><span class="sxs-lookup"><span data-stu-id="90e25-162">The existing certificate file path for the secondary cluster certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecSource

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e25-163">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="90e25-163">-SecondaryCertificatePassword</span></span>

<span data-ttu-id="90e25-164">인증서 파일의 암호</span><span class="sxs-lookup"><span data-stu-id="90e25-164">The password of the certificate file</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecCertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e25-165">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="90e25-165">-SecretIdentifier</span></span>

<span data-ttu-id="90e25-166">기존 Azure Key Vault 비밀 URL(예: https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f ''</span><span class="sxs-lookup"><span data-stu-id="90e25-166">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="90e25-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="90e25-167">-TemplateFile</span></span>

<span data-ttu-id="90e25-168">템플릿 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-168">The path to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e25-169">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="90e25-169">-Thumbprint</span></span>
<span data-ttu-id="90e25-170">SecretIdentifier에 대한 인증서 correspoinding에 대한 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-170">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="90e25-171">키 자격 증명 모음에 인증서만 비밀로 저장되고 cmdlet이 지문을 검색할 수 없는 경우 인증서가 관리되지 않는 경우 이 방법을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-171">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

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

### <span data-ttu-id="90e25-172">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="90e25-172">-VmPassword</span></span>

<span data-ttu-id="90e25-173">VM의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-173">The password of the Vm.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e25-174">-VmSku</span><span class="sxs-lookup"><span data-stu-id="90e25-174">-VmSku</span></span>

<span data-ttu-id="90e25-175">The Vm Sku</span><span class="sxs-lookup"><span data-stu-id="90e25-175">The Vm Sku</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: Sku

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e25-176">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="90e25-176">-VmUserName</span></span>

<span data-ttu-id="90e25-177">VM에 로깅하기 위한 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="90e25-177">The user name for logging to Vm</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e25-178">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90e25-178">-Confirm</span></span>

<span data-ttu-id="90e25-179">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90e25-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90e25-180">-WhatIf</span></span>

<span data-ttu-id="90e25-181">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="90e25-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90e25-182">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90e25-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e25-183">CommonParameters</span></span>
<span data-ttu-id="90e25-184">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="90e25-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e25-185">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="90e25-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e25-186">입력</span><span class="sxs-lookup"><span data-stu-id="90e25-186">INPUTS</span></span>

### <span data-ttu-id="90e25-187">System.String</span><span class="sxs-lookup"><span data-stu-id="90e25-187">System.String</span></span>

### <span data-ttu-id="90e25-188">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="90e25-188">System.Security.SecureString</span></span>

### <span data-ttu-id="90e25-189">System.Int32</span><span class="sxs-lookup"><span data-stu-id="90e25-189">System.Int32</span></span>

### <span data-ttu-id="90e25-190">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="90e25-190">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="90e25-191">출력</span><span class="sxs-lookup"><span data-stu-id="90e25-191">OUTPUTS</span></span>

### <span data-ttu-id="90e25-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="90e25-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="90e25-193">참고 사항</span><span class="sxs-lookup"><span data-stu-id="90e25-193">NOTES</span></span>

## <span data-ttu-id="90e25-194">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90e25-194">RELATED LINKS</span></span>
