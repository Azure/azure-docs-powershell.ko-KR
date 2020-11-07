---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
ms.openlocfilehash: e78912d2a8ab0ce4f5e990e69e236853a85019c6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699120"
---
# <span data-ttu-id="c0d68-101">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="c0d68-101">New-AzServiceFabricCluster</span></span>

## <span data-ttu-id="c0d68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0d68-102">SYNOPSIS</span></span>
<span data-ttu-id="c0d68-103">이 명령은 사용자가 제공 하는 인증서를 사용 하거나, 시스템에서 자체 서명 된 인증서를 생성 하 여 새 서비스 패브릭 클러스터를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="c0d68-104">제공 하는 기본 서식 파일 또는 사용자 지정 서식 파일을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="c0d68-105">자체 서명 된 인증서를 내보낼 폴더를 지정 하거나 나중에 키 자격 증명 모음에서 반입할 수 있는 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

## <span data-ttu-id="c0d68-106">구문과</span><span class="sxs-lookup"><span data-stu-id="c0d68-106">SYNTAX</span></span>

### <span data-ttu-id="c0d68-107">ByDefaultArmTemplate (기본값)</span><span class="sxs-lookup"><span data-stu-id="c0d68-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0d68-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="c0d68-108">ByExistingKeyVault</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0d68-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="c0d68-109">ByNewPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>]
 [-KeyVaultName <String>] [-CertificateSubjectName <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0d68-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="c0d68-110">ByExistingPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0d68-111">설명은</span><span class="sxs-lookup"><span data-stu-id="c0d68-111">DESCRIPTION</span></span>
<span data-ttu-id="c0d68-112">**AzServiceFabricCluster** 명령은 사용자가 제공 하는 인증서를 사용 하거나, 시스템에서 자체 서명 된 인증서를 생성 하 여 새 서비스 패브릭 클러스터를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-112">The **New-AzServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="c0d68-113">사용 되는 템플릿은 기본 서식 파일 또는 사용자 지정 서식 파일이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="c0d68-114">자체 서명 된 인증서를 내보낼 폴더를 지정 하거나 나중에 키 자격 증명 모음에서 반입할 수 있는 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="c0d68-115">사용자 지정 서식 파일과 매개 변수 파일을 지정 하는 경우에는 매개 변수 파일에 인증서 정보를 제공할 필요가 없으며 시스템에서 이러한 매개 변수를 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="c0d68-116">네 가지 옵션이 아래에 자세히 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-116">The four options are detailed below.</span></span> <span data-ttu-id="c0d68-117">각 매개 변수에 대 한 설명을 아래로 스크롤합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="c0d68-118">예제의</span><span class="sxs-lookup"><span data-stu-id="c0d68-118">EXAMPLES</span></span>

### <span data-ttu-id="c0d68-119">예제 1: 클러스터 크기, 인증서 주체 이름 및 클러스터를 배포할 OS만 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test01"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.cloudapp.azure.com" -f $RGname, $clusterloc
$pfxfolder="c:\certs"

Write-Output "Create cluster in '$clusterloc' with cert subject name '$subname' and cert output path '$pfxfolder'"

New-AzServiceFabricCluster -ResourceGroupName $RGname -Location $clusterloc -ClusterSize 5 -VmPassword $pass -CertificateSubjectName $subname -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="c0d68-120">이 명령은 클러스터 크기, 인증서 주체 이름 및 클러스터 배포 OS만 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="c0d68-121">예제 2: 키 보관소에 기존 인증서 리소스 지정 및 클러스터를 배포 하는 사용자 지정 서식 파일</span><span class="sxs-lookup"><span data-stu-id="c0d68-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>
```
$RGname="test20"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId="https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -SecretIdentifier $secretId
```

<span data-ttu-id="c0d68-122">이 명령은 키 자격 증명 모음에 기존 인증서 리소스를 지정 하 고 클러스터를 배포 하는 사용자 지정 템플릿을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="c0d68-123">예제 3: 사용자 지정 서식 파일을 사용 하 여 새 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="c0d68-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="c0d68-124">키 보관소에 다른 리소스 그룹 이름을 지정 하 고 시스템이 새 인증서를 업로드 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.$clusterloc.cloudapp.azure.com" -f $RGName, $clusterloc
$pfxfolder="~\Documents"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -KeyVaultResouceGroupName $keyVaultRG  -KeyVaultName $keyVault -CertificateSubjectName $subname
```

<span data-ttu-id="c0d68-125">이 명령은 사용자 지정 서식 파일을 사용 하 여 새 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="c0d68-126">키 보관소에 다른 리소스 그룹 이름을 지정 하 고 시스템이 새 인증서를 업로드 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="c0d68-127">예제 4: 자신의 인증서와 사용자 지정 서식 파일을 가져와 새 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="c0d68-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$pfxsourcefile="c:\Mycertificates\my2017Prodcert.pfx"
$templateParmfile="~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateFile $pfxsourcefile -CertificatePassword $pass -KeyVaultResouceGroupName $keyVaultRG -KeyVaultName $keyVault
```

<span data-ttu-id="c0d68-128">이 명령을 사용 하 여 고유한 인증서와 사용자 지정 서식 파일을 가져와 새 클러스터를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="c0d68-129">변수</span><span class="sxs-lookup"><span data-stu-id="c0d68-129">PARAMETERS</span></span>

### <span data-ttu-id="c0d68-130">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="c0d68-130">-CertificateCommonName</span></span>
<span data-ttu-id="c0d68-131">인증서 일반 이름</span><span class="sxs-lookup"><span data-stu-id="c0d68-131">Certificate common name</span></span>

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

### <span data-ttu-id="c0d68-132">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="c0d68-132">-CertificateFile</span></span>
<span data-ttu-id="c0d68-133">기본 클러스터 인증서에 대 한 기존 인증서 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-133">The existing certificate file path for the primary cluster certificate.</span></span>

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

### <span data-ttu-id="c0d68-134">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="c0d68-134">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="c0d68-135">인증서 발급자 지문 (두 개 이상 있는 경우 쉼표로 구분)</span><span class="sxs-lookup"><span data-stu-id="c0d68-135">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="c0d68-136">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="c0d68-136">-CertificateOutputFolder</span></span>
<span data-ttu-id="c0d68-137">만들려는 새 인증서 파일의 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-137">The folder of the new certificate file to be created.</span></span>

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

### <span data-ttu-id="c0d68-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c0d68-138">-CertificatePassword</span></span>
<span data-ttu-id="c0d68-139">인증서 파일의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-139">The password of the certificate file.</span></span>

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

### <span data-ttu-id="c0d68-140">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="c0d68-140">-CertificateSubjectName</span></span>
<span data-ttu-id="c0d68-141">만들려는 인증서의 주체 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-141">The subject name of the certificate to be created.</span></span>

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

### <span data-ttu-id="c0d68-142">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="c0d68-142">-ClusterSize</span></span>
<span data-ttu-id="c0d68-143">클러스터의 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-143">The number of nodes in the cluster.</span></span> <span data-ttu-id="c0d68-144">기본값은 5 노드입니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-144">Default are 5 nodes.</span></span>

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

### <span data-ttu-id="c0d68-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0d68-145">-DefaultProfile</span></span>
<span data-ttu-id="c0d68-146">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0d68-147">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="c0d68-147">-KeyVaultName</span></span>
<span data-ttu-id="c0d68-148">Azure 키 보관소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-148">Azure key vault name.</span></span> <span data-ttu-id="c0d68-149">제공 하지 않으면 기본적으로 리소스 그룹 이름으로 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-149">If not given, it will be defaulted to the resource group name.</span></span>

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

### <span data-ttu-id="c0d68-150">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0d68-150">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="c0d68-151">Azure 키 보관소 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-151">Azure key vault resource group name.</span></span> <span data-ttu-id="c0d68-152">지정 하지 않으면 기본적으로 리소스 그룹 이름이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-152">If not given, it will be defaulted to resource group name.</span></span>

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

### <span data-ttu-id="c0d68-153">-위치</span><span class="sxs-lookup"><span data-stu-id="c0d68-153">-Location</span></span>
<span data-ttu-id="c0d68-154">리소스 그룹 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-154">The resource group location.</span></span>

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

### <span data-ttu-id="c0d68-155">-이름</span><span class="sxs-lookup"><span data-stu-id="c0d68-155">-Name</span></span>
<span data-ttu-id="c0d68-156">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-156">Specify the name of the cluster.</span></span> <span data-ttu-id="c0d68-157">지정 하지 않으면 리소스 그룹 이름과 동일 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-157">If not given, it will be same as resource group name.</span></span>

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

### <span data-ttu-id="c0d68-158">-OS</span><span class="sxs-lookup"><span data-stu-id="c0d68-158">-OS</span></span>
<span data-ttu-id="c0d68-159">클러스터를 구성 하는 Vm의 운영 체제입니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-159">The Operating System of the VMs that make up the cluster.</span></span>

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

### <span data-ttu-id="c0d68-160">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="c0d68-160">-ParameterFile</span></span>
<span data-ttu-id="c0d68-161">Template 매개 변수 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-161">The path to the template parameter file.</span></span>

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

### <span data-ttu-id="c0d68-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0d68-162">-ResourceGroupName</span></span>
<span data-ttu-id="c0d68-163">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-163">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c0d68-164">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="c0d68-164">-SecondaryCertificateFile</span></span>
<span data-ttu-id="c0d68-165">보조 클러스터 인증서에 대 한 기존 인증서 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-165">The existing certificate file path for the secondary cluster certificate.</span></span>

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

### <span data-ttu-id="c0d68-166">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c0d68-166">-SecondaryCertificatePassword</span></span>
<span data-ttu-id="c0d68-167">인증서 파일의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-167">The password of the certificate file.</span></span>

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

### <span data-ttu-id="c0d68-168">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="c0d68-168">-SecretIdentifier</span></span>
<span data-ttu-id="c0d68-169">기존 Azure 키 자격 증명 모음 비밀 URL (예: ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f ').</span><span class="sxs-lookup"><span data-stu-id="c0d68-169">The existing Azure key vault secret URL, for example: 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'.</span></span>

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

### <span data-ttu-id="c0d68-170">-서식 파일</span><span class="sxs-lookup"><span data-stu-id="c0d68-170">-TemplateFile</span></span>
<span data-ttu-id="c0d68-171">서식 파일에 대 한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-171">The path to the template file.</span></span>

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

### <span data-ttu-id="c0d68-172">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="c0d68-172">-VmPassword</span></span>
<span data-ttu-id="c0d68-173">Vm의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-173">The password of the Vm.</span></span>

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

### <span data-ttu-id="c0d68-174">-VmSku</span><span class="sxs-lookup"><span data-stu-id="c0d68-174">-VmSku</span></span>
<span data-ttu-id="c0d68-175">Vm Sku.</span><span class="sxs-lookup"><span data-stu-id="c0d68-175">The Vm Sku.</span></span>

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

### <span data-ttu-id="c0d68-176">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="c0d68-176">-VmUserName</span></span>
<span data-ttu-id="c0d68-177">Vm에 로깅하는 데 사용 되는 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-177">The user name for logging to Vm.</span></span>

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

### <span data-ttu-id="c0d68-178">-확인</span><span class="sxs-lookup"><span data-stu-id="c0d68-178">-Confirm</span></span>
<span data-ttu-id="c0d68-179">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0d68-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0d68-180">-WhatIf</span></span>
<span data-ttu-id="c0d68-181">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-181">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0d68-182">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0d68-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0d68-183">CommonParameters</span></span>
<span data-ttu-id="c0d68-184">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d68-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0d68-185">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0d68-185">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0d68-186">입력</span><span class="sxs-lookup"><span data-stu-id="c0d68-186">INPUTS</span></span>

### <span data-ttu-id="c0d68-187">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c0d68-187">System.String</span></span>

### <span data-ttu-id="c0d68-188">System.webserver</span><span class="sxs-lookup"><span data-stu-id="c0d68-188">System.Security.SecureString</span></span>

### <span data-ttu-id="c0d68-189">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="c0d68-189">System.Int32</span></span>

### <span data-ttu-id="c0d68-190">ServiceFabric. a. i m/.</span><span class="sxs-lookup"><span data-stu-id="c0d68-190">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="c0d68-191">출력</span><span class="sxs-lookup"><span data-stu-id="c0d68-191">OUTPUTS</span></span>

### <span data-ttu-id="c0d68-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="c0d68-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="c0d68-193">상속자</span><span class="sxs-lookup"><span data-stu-id="c0d68-193">NOTES</span></span>

## <span data-ttu-id="c0d68-194">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0d68-194">RELATED LINKS</span></span>
