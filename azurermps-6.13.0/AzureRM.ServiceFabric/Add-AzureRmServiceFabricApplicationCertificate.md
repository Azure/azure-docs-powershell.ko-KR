---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricapplicationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
ms.openlocfilehash: 982eb6bf8c579d3f6ef9a5c6b74299ecf1114eb6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529368"
---
# <span data-ttu-id="c7666-101">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="c7666-101">Add-AzureRmServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="c7666-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7666-102">SYNOPSIS</span></span>
<span data-ttu-id="c7666-103">클러스터를 구성 하는 가상 컴퓨터 크기 집합에 새 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7666-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="c7666-104">인증서는 응용 프로그램 인증서로 사용 하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c7666-104">The certificate is intended to be used as an application certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7666-105">구문과</span><span class="sxs-lookup"><span data-stu-id="c7666-105">SYNTAX</span></span>

### <span data-ttu-id="c7666-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="c7666-106">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7666-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="c7666-107">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7666-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="c7666-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7666-109">설명은</span><span class="sxs-lookup"><span data-stu-id="c7666-109">DESCRIPTION</span></span>
<span data-ttu-id="c7666-110">**Add-AzureRmServiceFabricApplicationCertificate** 를 사용 하 여 클러스터의 모든 노드에 인증서를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7666-110">Use **Add-AzureRmServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="c7666-111">이미 보유 하 고 있는 인증서를 지정 하거나 시스템에서 새 항목을 생성 하도록 설정한 다음 새 또는 기존 Azure 키 자격 증명 모음에 업로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7666-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="c7666-112">예제의</span><span class="sxs-lookup"><span data-stu-id="c7666-112">EXAMPLES</span></span>

### <span data-ttu-id="c7666-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="c7666-113">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="c7666-114">이 명령은 클러스터의 모든 노드 형식에 기존 Azure key vault의 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7666-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="c7666-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="c7666-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="c7666-116">이 명령은 키 보관소 리소스 그룹 이름 및 키 보관소 이름을 사용 하 여 Azure key vault에 자체 서명 된 인증서를 만들고, 클러스터의 모든 노드 형식에 설치 하 고, ' c:\test ' 폴더에서 인증서를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7666-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="c7666-117">다운로드 한 인증서 이름은 키 보관소 인증서의 이름과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c7666-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="c7666-118">변수</span><span class="sxs-lookup"><span data-stu-id="c7666-118">PARAMETERS</span></span>

### <span data-ttu-id="c7666-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="c7666-119">-CertificateFile</span></span>
<span data-ttu-id="c7666-120">기존 인증서 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c7666-120">The existing certificate file path.</span></span>

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

### <span data-ttu-id="c7666-121">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="c7666-121">-CertificateOutputFolder</span></span>
<span data-ttu-id="c7666-122">만들려는 새 인증서의 폴더 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c7666-122">The folder path of the new certificate to be created.</span></span>

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

### <span data-ttu-id="c7666-123">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c7666-123">-CertificatePassword</span></span>
<span data-ttu-id="c7666-124">Pfx 파일의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="c7666-124">The password of the pfx file.</span></span>

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

### <span data-ttu-id="c7666-125">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="c7666-125">-CertificateSubjectName</span></span>
<span data-ttu-id="c7666-126">만들려는 인증서의 Dns 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7666-126">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="c7666-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7666-127">-DefaultProfile</span></span>
<span data-ttu-id="c7666-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7666-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7666-129">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="c7666-129">-KeyVaultName</span></span>
<span data-ttu-id="c7666-130">Azure 키 보관소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7666-130">Azure key vault name.</span></span>

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

### <span data-ttu-id="c7666-131">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7666-131">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="c7666-132">Azure 키 보관소 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7666-132">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="c7666-133">-이름</span><span class="sxs-lookup"><span data-stu-id="c7666-133">-Name</span></span>
<span data-ttu-id="c7666-134">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7666-134">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c7666-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7666-135">-ResourceGroupName</span></span>
<span data-ttu-id="c7666-136">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7666-136">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c7666-137">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="c7666-137">-SecretIdentifier</span></span>
<span data-ttu-id="c7666-138">기존 Azure 키 자격 증명 모음 비밀 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="c7666-138">The existing Azure key vault secret uri.</span></span>

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

### <span data-ttu-id="c7666-139">-확인</span><span class="sxs-lookup"><span data-stu-id="c7666-139">-Confirm</span></span>
<span data-ttu-id="c7666-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7666-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7666-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7666-141">-WhatIf</span></span>
<span data-ttu-id="c7666-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c7666-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7666-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7666-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7666-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7666-144">CommonParameters</span></span>
<span data-ttu-id="c7666-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7666-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7666-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7666-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7666-147">입력</span><span class="sxs-lookup"><span data-stu-id="c7666-147">INPUTS</span></span>

### <span data-ttu-id="c7666-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c7666-148">System.String</span></span>
<span data-ttu-id="c7666-149">매개 변수: CertificateFile (ByValue), CertificateOutputFolder (ByValue), CertificateSubjectName (ByValue), KeyVaultName (ByValue), KeyVaultResouceGroupName (byvalue), SecretIdentifier (byvalue)</span><span class="sxs-lookup"><span data-stu-id="c7666-149">Parameters: CertificateFile (ByValue), CertificateOutputFolder (ByValue), CertificateSubjectName (ByValue), KeyVaultName (ByValue), KeyVaultResouceGroupName (ByValue), SecretIdentifier (ByValue)</span></span>

### <span data-ttu-id="c7666-150">System.webserver</span><span class="sxs-lookup"><span data-stu-id="c7666-150">System.Security.SecureString</span></span>
<span data-ttu-id="c7666-151">매개 변수: CertificatePassword (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c7666-151">Parameters: CertificatePassword (ByValue)</span></span>

## <span data-ttu-id="c7666-152">출력</span><span class="sxs-lookup"><span data-stu-id="c7666-152">OUTPUTS</span></span>

### <span data-ttu-id="c7666-153">ServiceFabric. PSKeyVault.</span><span class="sxs-lookup"><span data-stu-id="c7666-153">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="c7666-154">상속자</span><span class="sxs-lookup"><span data-stu-id="c7666-154">NOTES</span></span>

## <span data-ttu-id="c7666-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7666-155">RELATED LINKS</span></span>

[<span data-ttu-id="c7666-156">추가-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="c7666-156">Add-AzureRmServiceFabricClusterCertificate</span></span>](./Add-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="c7666-157">새로운 AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="c7666-157">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)
