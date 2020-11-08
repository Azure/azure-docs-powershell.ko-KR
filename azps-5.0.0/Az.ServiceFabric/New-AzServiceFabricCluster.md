---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
ms.openlocfilehash: 9e5ba2d2ee228da30a887c0c7b318dd9d270d763
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226175"
---
# <span data-ttu-id="7677f-101">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="7677f-101">New-AzServiceFabricCluster</span></span>

## <span data-ttu-id="7677f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7677f-102">SYNOPSIS</span></span>

<span data-ttu-id="7677f-103">이 명령은 사용자가 제공 하는 인증서를 사용 하거나, 시스템에서 자체 서명 된 인증서를 생성 하 여 새 서비스 패브릭 클러스터를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="7677f-104">제공 하는 기본 서식 파일 또는 사용자 지정 서식 파일을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="7677f-105">자체 서명 된 인증서를 내보낼 폴더를 지정 하거나 나중에 키 자격 증명 모음에서 반입할 수 있는 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

## <span data-ttu-id="7677f-106">구문과</span><span class="sxs-lookup"><span data-stu-id="7677f-106">SYNTAX</span></span>

### <span data-ttu-id="7677f-107">ByDefaultArmTemplate (기본값)</span><span class="sxs-lookup"><span data-stu-id="7677f-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7677f-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="7677f-108">ByExistingKeyVault</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 -SecretIdentifier <String> [-Thumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7677f-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="7677f-109">ByNewPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>]
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateSubjectName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7677f-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="7677f-110">ByExistingPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7677f-111">설명은</span><span class="sxs-lookup"><span data-stu-id="7677f-111">DESCRIPTION</span></span>

<span data-ttu-id="7677f-112">**AzServiceFabricCluster** 명령은 사용자가 제공 하는 인증서를 사용 하거나, 시스템에서 자체 서명 된 인증서를 생성 하 여 새 서비스 패브릭 클러스터를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-112">The **New-AzServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="7677f-113">사용 되는 템플릿은 기본 서식 파일 또는 사용자 지정 서식 파일이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="7677f-114">자체 서명 된 인증서를 내보낼 폴더를 지정 하거나 나중에 키 자격 증명 모음에서 반입할 수 있는 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="7677f-115">사용자 지정 서식 파일과 매개 변수 파일을 지정 하는 경우에는 매개 변수 파일에 인증서 정보를 제공할 필요가 없으며 시스템에서 이러한 매개 변수를 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="7677f-116">네 가지 옵션이 아래에 자세히 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-116">The four options are detailed below.</span></span> <span data-ttu-id="7677f-117">각 매개 변수에 대 한 설명을 아래로 스크롤합니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="7677f-118">예제의</span><span class="sxs-lookup"><span data-stu-id="7677f-118">EXAMPLES</span></span>

### <span data-ttu-id="7677f-119">예제 1: 클러스터 크기, 인증서 주체 이름 및 클러스터를 배포할 OS만 지정</span><span class="sxs-lookup"><span data-stu-id="7677f-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -f $resourceGroupName, $azureRegion
$localCertificateFolder = "c:\certs"

Write-Output "Create cluster in '$azureRegion' with cert subject name '$clusterDnsName' and cert output path '$localCertificateFolder'"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -Location $azureRegion -ClusterSize 5 -VmPassword $password -CertificateSubjectName $clusterDnsName -CertificateOutputFolder $localCertificateFolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="7677f-120">이 명령은 클러스터 크기, 인증서 주체 이름 및 클러스터 배포 OS만 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="7677f-121">예제 2: 키 보관소에 기존 인증서 리소스 지정 및 클러스터를 배포 하는 사용자 지정 서식 파일</span><span class="sxs-lookup"><span data-stu-id="7677f-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>

```powershell
$resourceGroupName = "test20"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId = "https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -SecretIdentifier $secretId
```

<span data-ttu-id="7677f-122">이 명령은 키 자격 증명 모음에 기존 인증서 리소스를 지정 하 고 클러스터를 배포 하는 사용자 지정 템플릿을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="7677f-123">예제 3: 사용자 지정 서식 파일을 사용 하 여 새 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="7677f-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="7677f-124">키 보관소에 다른 리소스 그룹 이름을 지정 하 고 시스템이 새 인증서를 업로드 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

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

<span data-ttu-id="7677f-125">이 명령은 사용자 지정 서식 파일을 사용 하 여 새 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="7677f-126">키 보관소에 다른 리소스 그룹 이름을 지정 하 고 시스템이 새 인증서를 업로드 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="7677f-127">예제 4: 자신의 인증서와 사용자 지정 서식 파일을 가져와 새 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="7677f-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>

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

<span data-ttu-id="7677f-128">이 명령을 사용 하 여 고유한 인증서와 사용자 지정 서식 파일을 가져와 새 클러스터를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="7677f-129">변수</span><span class="sxs-lookup"><span data-stu-id="7677f-129">PARAMETERS</span></span>

### <span data-ttu-id="7677f-130">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="7677f-130">-CertificateCommonName</span></span>

<span data-ttu-id="7677f-131">인증서 일반 이름</span><span class="sxs-lookup"><span data-stu-id="7677f-131">Certificate common name</span></span>

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

### <span data-ttu-id="7677f-132">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="7677f-132">-CertificateFile</span></span>

<span data-ttu-id="7677f-133">기본 클러스터 인증서에 대 한 기존 인증서 파일 경로</span><span class="sxs-lookup"><span data-stu-id="7677f-133">The existing certificate file path for the primary cluster certificate</span></span>

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

### <span data-ttu-id="7677f-134">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="7677f-134">-CertificateIssuerThumbprint</span></span>

<span data-ttu-id="7677f-135">인증서 발급자 지문 (두 개 이상 있는 경우 쉼표로 구분)</span><span class="sxs-lookup"><span data-stu-id="7677f-135">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="7677f-136">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="7677f-136">-CertificateOutputFolder</span></span>

<span data-ttu-id="7677f-137">만들 새 인증서 파일의 폴더</span><span class="sxs-lookup"><span data-stu-id="7677f-137">The folder of the new certificate file to be created</span></span>

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

### <span data-ttu-id="7677f-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="7677f-138">-CertificatePassword</span></span>

<span data-ttu-id="7677f-139">인증서 파일의 암호</span><span class="sxs-lookup"><span data-stu-id="7677f-139">The password of the certificate file</span></span>

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

### <span data-ttu-id="7677f-140">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="7677f-140">-CertificateSubjectName</span></span>

<span data-ttu-id="7677f-141">만들려는 인증서의 주체 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-141">The subject name of the certificate to be created</span></span>

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

### <span data-ttu-id="7677f-142">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="7677f-142">-ClusterSize</span></span>

<span data-ttu-id="7677f-143">클러스터의 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-143">The number of nodes in the cluster.</span></span>
<span data-ttu-id="7677f-144">기본값은 5 개 노드입니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-144">Default are 5 nodes</span></span>

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

### <span data-ttu-id="7677f-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7677f-145">-DefaultProfile</span></span>

<span data-ttu-id="7677f-146">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7677f-147">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="7677f-147">-KeyVaultName</span></span>

<span data-ttu-id="7677f-148">Azure 키 자격 증명 모음 이름 (지정 하지 않으면 기본적으로 리소스 그룹 이름으로 됨)</span><span class="sxs-lookup"><span data-stu-id="7677f-148">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="7677f-149">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7677f-149">-KeyVaultResourceGroupName</span></span>

<span data-ttu-id="7677f-150">Azure 키 자격 증명 모음 리소스 그룹 이름입니다. 지정 하지 않으면 기본적으로 리소스 그룹 이름이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-150">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="7677f-151">-위치</span><span class="sxs-lookup"><span data-stu-id="7677f-151">-Location</span></span>

<span data-ttu-id="7677f-152">리소스 그룹 위치</span><span class="sxs-lookup"><span data-stu-id="7677f-152">The resource group location</span></span>

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

### <span data-ttu-id="7677f-153">-이름</span><span class="sxs-lookup"><span data-stu-id="7677f-153">-Name</span></span>

<span data-ttu-id="7677f-154">클러스터의 이름을 지정 하지 않으면 리소스 그룹 이름과 동일 하 게 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-154">Specify the name of the cluster, if not given it will be same as resource group name</span></span>

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

### <span data-ttu-id="7677f-155">-OS</span><span class="sxs-lookup"><span data-stu-id="7677f-155">-OS</span></span>

<span data-ttu-id="7677f-156">클러스터를 구성 하는 Vm의 운영 체제입니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-156">The Operating System of the VMs that make up the cluster.</span></span>

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

### <span data-ttu-id="7677f-157">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="7677f-157">-ParameterFile</span></span>

<span data-ttu-id="7677f-158">Template 매개 변수 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-158">The path to the template parameter file.</span></span>

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

### <span data-ttu-id="7677f-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7677f-159">-ResourceGroupName</span></span>

<span data-ttu-id="7677f-160">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-160">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="7677f-161">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="7677f-161">-SecondaryCertificateFile</span></span>

<span data-ttu-id="7677f-162">보조 클러스터 인증서에 대 한 기존 인증서 파일 경로</span><span class="sxs-lookup"><span data-stu-id="7677f-162">The existing certificate file path for the secondary cluster certificate</span></span>

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

### <span data-ttu-id="7677f-163">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="7677f-163">-SecondaryCertificatePassword</span></span>

<span data-ttu-id="7677f-164">인증서 파일의 암호</span><span class="sxs-lookup"><span data-stu-id="7677f-164">The password of the certificate file</span></span>

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

### <span data-ttu-id="7677f-165">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="7677f-165">-SecretIdentifier</span></span>

<span data-ttu-id="7677f-166">기존 Azure 키 자격 증명 모음 비밀 URL (예: ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f ')</span><span class="sxs-lookup"><span data-stu-id="7677f-166">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="7677f-167">-서식 파일</span><span class="sxs-lookup"><span data-stu-id="7677f-167">-TemplateFile</span></span>

<span data-ttu-id="7677f-168">서식 파일에 대 한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-168">The path to the template file.</span></span>

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

### <span data-ttu-id="7677f-169">-지문</span><span class="sxs-lookup"><span data-stu-id="7677f-169">-Thumbprint</span></span>
<span data-ttu-id="7677f-170">인증서에 대 한 지문이 SecretIdentifier에 correspoinding.</span><span class="sxs-lookup"><span data-stu-id="7677f-170">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="7677f-171">키 자격 증명 모음이 비밀으로 저장 된 인증서만 있고 cmdlet에서 지문을 검색할 수 없는 경우에는 인증서가 관리 되지 않는 경우이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-171">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

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

### <span data-ttu-id="7677f-172">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="7677f-172">-VmPassword</span></span>

<span data-ttu-id="7677f-173">Vm의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-173">The password of the Vm.</span></span>

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

### <span data-ttu-id="7677f-174">-VmSku</span><span class="sxs-lookup"><span data-stu-id="7677f-174">-VmSku</span></span>

<span data-ttu-id="7677f-175">Vm Sku</span><span class="sxs-lookup"><span data-stu-id="7677f-175">The Vm Sku</span></span>

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

### <span data-ttu-id="7677f-176">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="7677f-176">-VmUserName</span></span>

<span data-ttu-id="7677f-177">Vm에 로깅하는 데 사용할 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-177">The user name for logging to Vm</span></span>

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

### <span data-ttu-id="7677f-178">-확인</span><span class="sxs-lookup"><span data-stu-id="7677f-178">-Confirm</span></span>

<span data-ttu-id="7677f-179">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7677f-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7677f-180">-WhatIf</span></span>

<span data-ttu-id="7677f-181">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7677f-182">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7677f-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7677f-183">CommonParameters</span></span>
<span data-ttu-id="7677f-184">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7677f-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7677f-185">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7677f-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7677f-186">입력</span><span class="sxs-lookup"><span data-stu-id="7677f-186">INPUTS</span></span>

### <span data-ttu-id="7677f-187">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7677f-187">System.String</span></span>

### <span data-ttu-id="7677f-188">System.webserver</span><span class="sxs-lookup"><span data-stu-id="7677f-188">System.Security.SecureString</span></span>

### <span data-ttu-id="7677f-189">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="7677f-189">System.Int32</span></span>

### <span data-ttu-id="7677f-190">ServiceFabric. a. i m/.</span><span class="sxs-lookup"><span data-stu-id="7677f-190">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="7677f-191">출력</span><span class="sxs-lookup"><span data-stu-id="7677f-191">OUTPUTS</span></span>

### <span data-ttu-id="7677f-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="7677f-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="7677f-193">상속자</span><span class="sxs-lookup"><span data-stu-id="7677f-193">NOTES</span></span>

## <span data-ttu-id="7677f-194">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7677f-194">RELATED LINKS</span></span>
