---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
ms.openlocfilehash: 6d77c795415bca1a8bffbed6d09062f394782e94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535420"
---
# <span data-ttu-id="c7259-101">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="c7259-101">Add-AzureRmServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="c7259-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7259-102">SYNOPSIS</span></span>
<span data-ttu-id="c7259-103">클러스터를 구성 하는 가상 컴퓨터 크기 집합에 새 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7259-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="c7259-104">인증서는 응용 프로그램 인증서로 사용 하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c7259-104">The certificate is intended to be used as an application certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7259-105">구문과</span><span class="sxs-lookup"><span data-stu-id="c7259-105">SYNTAX</span></span>

### <span data-ttu-id="c7259-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="c7259-106">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7259-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="c7259-107">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7259-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="c7259-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7259-109">설명은</span><span class="sxs-lookup"><span data-stu-id="c7259-109">DESCRIPTION</span></span>
<span data-ttu-id="c7259-110">**Add-AzureRmServiceFabricApplicationCertificate** 를 사용 하 여 클러스터의 모든 노드에 인증서를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7259-110">Use **Add-AzureRmServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="c7259-111">이미 보유 하 고 있는 인증서를 지정 하거나 시스템에서 새 항목을 생성 하도록 설정한 다음 새 또는 기존 Azure 키 자격 증명 모음에 업로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7259-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="c7259-112">예제의</span><span class="sxs-lookup"><span data-stu-id="c7259-112">EXAMPLES</span></span>

### <span data-ttu-id="c7259-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="c7259-113">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="c7259-114">이 명령은 클러스터의 모든 노드 형식에 기존 Azure key vault의 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7259-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="c7259-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="c7259-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="c7259-116">이 명령은 키 보관소 리소스 그룹 이름 및 키 보관소 이름을 사용 하 여 Azure key vault에 자체 서명 된 인증서를 만들고, 클러스터의 모든 노드 형식에 설치 하 고, ' c:\test ' 폴더에서 인증서를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7259-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="c7259-117">다운로드 한 인증서 이름은 키 보관소 인증서의 이름과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c7259-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="c7259-118">변수</span><span class="sxs-lookup"><span data-stu-id="c7259-118">PARAMETERS</span></span>

### <span data-ttu-id="c7259-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="c7259-119">-CertificateFile</span></span>
<span data-ttu-id="c7259-120">기존 인증서 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c7259-120">The existing certificate file path.</span></span>

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

### <span data-ttu-id="c7259-121">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="c7259-121">-CertificateOutputFolder</span></span>
<span data-ttu-id="c7259-122">만들려는 새 인증서의 폴더 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c7259-122">The folder path of the new certificate to be created.</span></span>

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

### <span data-ttu-id="c7259-123">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c7259-123">-CertificatePassword</span></span>
<span data-ttu-id="c7259-124">Pfx 파일의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="c7259-124">The password of the pfx file.</span></span>

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

### <span data-ttu-id="c7259-125">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="c7259-125">-CertificateSubjectName</span></span>
<span data-ttu-id="c7259-126">만들려는 인증서의 Dns 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7259-126">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="c7259-127">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="c7259-127">-KeyVaultName</span></span>
<span data-ttu-id="c7259-128">Azure 키 보관소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7259-128">Azure key vault name.</span></span>

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

### <span data-ttu-id="c7259-129">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7259-129">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="c7259-130">Azure 키 보관소 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7259-130">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="c7259-131">-이름</span><span class="sxs-lookup"><span data-stu-id="c7259-131">-Name</span></span>
<span data-ttu-id="c7259-132">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7259-132">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c7259-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7259-133">-ResourceGroupName</span></span>
<span data-ttu-id="c7259-134">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7259-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c7259-135">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="c7259-135">-SecretIdentifier</span></span>
<span data-ttu-id="c7259-136">기존 Azure 키 자격 증명 모음 비밀 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="c7259-136">The existing Azure key vault secret uri.</span></span>

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

### <span data-ttu-id="c7259-137">-확인</span><span class="sxs-lookup"><span data-stu-id="c7259-137">-Confirm</span></span>
<span data-ttu-id="c7259-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7259-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7259-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7259-139">-WhatIf</span></span>
<span data-ttu-id="c7259-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c7259-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7259-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7259-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7259-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7259-142">-DefaultProfile</span></span>
<span data-ttu-id="c7259-143">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7259-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7259-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7259-144">CommonParameters</span></span>
<span data-ttu-id="c7259-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7259-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7259-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7259-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7259-147">입력</span><span class="sxs-lookup"><span data-stu-id="c7259-147">INPUTS</span></span>

### <span data-ttu-id="c7259-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c7259-148">System.String</span></span>

## <span data-ttu-id="c7259-149">출력</span><span class="sxs-lookup"><span data-stu-id="c7259-149">OUTPUTS</span></span>

### <span data-ttu-id="c7259-150">ServiceFabric. PSKeyVault.</span><span class="sxs-lookup"><span data-stu-id="c7259-150">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="c7259-151">상속자</span><span class="sxs-lookup"><span data-stu-id="c7259-151">NOTES</span></span>

## <span data-ttu-id="c7259-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7259-152">RELATED LINKS</span></span>

[<span data-ttu-id="c7259-153">추가-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="c7259-153">Add-AzureRmServiceFabricClusterCertificate</span></span>](./Add-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="c7259-154">새로운 AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="c7259-154">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)
