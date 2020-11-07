---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricapplicationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
ms.openlocfilehash: 62298a5747a8bb5b4f01458cac611f5e86869ee7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873082"
---
# <span data-ttu-id="ed15b-101">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="ed15b-101">Add-AzServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="ed15b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed15b-102">SYNOPSIS</span></span>
<span data-ttu-id="ed15b-103">클러스터를 구성 하는 가상 컴퓨터 크기 집합에 새 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed15b-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="ed15b-104">인증서는 응용 프로그램 인증서로 사용 하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ed15b-104">The certificate is intended to be used as an application certificate.</span></span>

## <span data-ttu-id="ed15b-105">구문과</span><span class="sxs-lookup"><span data-stu-id="ed15b-105">SYNTAX</span></span>

### <span data-ttu-id="ed15b-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="ed15b-106">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed15b-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="ed15b-107">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed15b-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="ed15b-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed15b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="ed15b-109">DESCRIPTION</span></span>
<span data-ttu-id="ed15b-110">**Add-AzServiceFabricApplicationCertificate** 를 사용 하 여 클러스터의 모든 노드에 인증서를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed15b-110">Use **Add-AzServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="ed15b-111">이미 보유 하 고 있는 인증서를 지정 하거나 시스템에서 새 항목을 생성 하도록 설정한 다음 새 또는 기존 Azure 키 자격 증명 모음에 업로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed15b-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="ed15b-112">예제의</span><span class="sxs-lookup"><span data-stu-id="ed15b-112">EXAMPLES</span></span>

### <span data-ttu-id="ed15b-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="ed15b-113">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="ed15b-114">이 명령은 클러스터의 모든 노드 형식에 기존 Azure key vault의 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed15b-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="ed15b-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="ed15b-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="ed15b-116">이 명령은 키 보관소 리소스 그룹 이름 및 키 보관소 이름을 사용 하 여 Azure key vault에 자체 서명 된 인증서를 만들고, 클러스터의 모든 노드 형식에 설치 하 고, ' c:\test ' 폴더에서 인증서를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed15b-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="ed15b-117">다운로드 한 인증서 이름은 키 보관소 인증서의 이름과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ed15b-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="ed15b-118">변수</span><span class="sxs-lookup"><span data-stu-id="ed15b-118">PARAMETERS</span></span>

### <span data-ttu-id="ed15b-119">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="ed15b-119">-CertificateCommonName</span></span>
<span data-ttu-id="ed15b-120">인증서 일반 이름</span><span class="sxs-lookup"><span data-stu-id="ed15b-120">Certificate common name</span></span>

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

### <span data-ttu-id="ed15b-121">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="ed15b-121">-CertificateFile</span></span>
<span data-ttu-id="ed15b-122">기존 인증서의 경로</span><span class="sxs-lookup"><span data-stu-id="ed15b-122">The path to the existing certificate</span></span>

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

### <span data-ttu-id="ed15b-123">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="ed15b-123">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="ed15b-124">인증서 발급자 지문 (두 개 이상 있는 경우 쉼표로 구분)</span><span class="sxs-lookup"><span data-stu-id="ed15b-124">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="ed15b-125">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="ed15b-125">-CertificateOutputFolder</span></span>
<span data-ttu-id="ed15b-126">새 인증서를 다운로드 해야 하는 폴더</span><span class="sxs-lookup"><span data-stu-id="ed15b-126">The folder where the new certificate needs to be downloaded.</span></span>

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

### <span data-ttu-id="ed15b-127">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="ed15b-127">-CertificatePassword</span></span>
<span data-ttu-id="ed15b-128">인증서의 암호</span><span class="sxs-lookup"><span data-stu-id="ed15b-128">The password of the certificate</span></span>

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

### <span data-ttu-id="ed15b-129">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="ed15b-129">-CertificateSubjectName</span></span>
<span data-ttu-id="ed15b-130">인증서의 주체 이름</span><span class="sxs-lookup"><span data-stu-id="ed15b-130">The subject name of the certificate</span></span>

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

### <span data-ttu-id="ed15b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed15b-131">-DefaultProfile</span></span>
<span data-ttu-id="ed15b-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed15b-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed15b-133">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="ed15b-133">-KeyVaultName</span></span>
<span data-ttu-id="ed15b-134">Azure 키 자격 증명 모음 이름 (지정 하지 않으면 기본적으로 리소스 그룹 이름으로 됨)</span><span class="sxs-lookup"><span data-stu-id="ed15b-134">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="ed15b-135">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed15b-135">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="ed15b-136">Azure 키 자격 증명 모음 리소스 그룹 이름입니다. 지정 하지 않으면 기본적으로 리소스 그룹 이름이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed15b-136">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="ed15b-137">-이름</span><span class="sxs-lookup"><span data-stu-id="ed15b-137">-Name</span></span>
<span data-ttu-id="ed15b-138">클러스터 이름 지정</span><span class="sxs-lookup"><span data-stu-id="ed15b-138">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="ed15b-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed15b-139">-ResourceGroupName</span></span>
<span data-ttu-id="ed15b-140">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed15b-140">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ed15b-141">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="ed15b-141">-SecretIdentifier</span></span>
<span data-ttu-id="ed15b-142">기존 Azure 키 자격 증명 모음 비밀 URL (예: ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f ')</span><span class="sxs-lookup"><span data-stu-id="ed15b-142">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="ed15b-143">-확인</span><span class="sxs-lookup"><span data-stu-id="ed15b-143">-Confirm</span></span>
<span data-ttu-id="ed15b-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed15b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed15b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed15b-145">-WhatIf</span></span>
<span data-ttu-id="ed15b-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ed15b-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed15b-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed15b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed15b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed15b-148">CommonParameters</span></span>
<span data-ttu-id="ed15b-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed15b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed15b-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed15b-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed15b-151">입력</span><span class="sxs-lookup"><span data-stu-id="ed15b-151">INPUTS</span></span>

### <span data-ttu-id="ed15b-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ed15b-152">System.String</span></span>

### <span data-ttu-id="ed15b-153">System.webserver</span><span class="sxs-lookup"><span data-stu-id="ed15b-153">System.Security.SecureString</span></span>

## <span data-ttu-id="ed15b-154">출력</span><span class="sxs-lookup"><span data-stu-id="ed15b-154">OUTPUTS</span></span>

### <span data-ttu-id="ed15b-155">ServiceFabric. PSKeyVault.</span><span class="sxs-lookup"><span data-stu-id="ed15b-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="ed15b-156">상속자</span><span class="sxs-lookup"><span data-stu-id="ed15b-156">NOTES</span></span>

## <span data-ttu-id="ed15b-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed15b-157">RELATED LINKS</span></span>

[<span data-ttu-id="ed15b-158">추가-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="ed15b-158">Add-AzServiceFabricClusterCertificate</span></span>](./Add-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="ed15b-159">새로운 AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="ed15b-159">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
