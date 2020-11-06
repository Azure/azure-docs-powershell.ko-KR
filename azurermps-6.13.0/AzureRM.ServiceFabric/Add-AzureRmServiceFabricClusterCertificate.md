---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: fa357a4f5b8e599858ce5aff3e0aa11121833ba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530890"
---
# <span data-ttu-id="fafbf-101">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="fafbf-101">Add-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="fafbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fafbf-102">SYNOPSIS</span></span>
<span data-ttu-id="fafbf-103">클러스터에 보조 클러스터 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fafbf-103">Add a secondary cluster certificate to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fafbf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fafbf-104">SYNTAX</span></span>

### <span data-ttu-id="fafbf-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="fafbf-105">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fafbf-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="fafbf-106">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fafbf-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="fafbf-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fafbf-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fafbf-108">DESCRIPTION</span></span>
<span data-ttu-id="fafbf-109">**추가-AzureRmServiceFabricClusterCertificate** 를 사용 하 여 기존 azure 키 자격 증명 모음에서 보조 클러스터 인증서를 추가 하거나 제공 된 기존 인증서를 사용 하 여 새 azure 키 자격 증명 모음을 만들거나, 만든 새 인증서에서 생성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fafbf-109">Use **Add-AzureRmServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="fafbf-110">보조 클러스터가 있으면이를 재정의 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fafbf-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="fafbf-111">예제의</span><span class="sxs-lookup"><span data-stu-id="fafbf-111">EXAMPLES</span></span>

### <span data-ttu-id="fafbf-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="fafbf-112">Example 1</span></span>
```
Add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="fafbf-113">이 명령은 기존 Azure key 자격 증명 모음에 보조 클러스터 인증서로 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fafbf-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="fafbf-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="fafbf-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="fafbf-115">이 명령은 Azure key vault에 자체 서명 된 인증서를 만들고 보조 클러스터 인증서로 사용 하도록 클러스터를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fafbf-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="fafbf-116">변수</span><span class="sxs-lookup"><span data-stu-id="fafbf-116">PARAMETERS</span></span>

### <span data-ttu-id="fafbf-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="fafbf-117">-CertificateFile</span></span>
<span data-ttu-id="fafbf-118">기존 인증서 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="fafbf-118">The existing certificate file path.</span></span>

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

### <span data-ttu-id="fafbf-119">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="fafbf-119">-CertificateOutputFolder</span></span>
<span data-ttu-id="fafbf-120">만들려는 새 인증서의 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="fafbf-120">The folder of the new certificate to be created.</span></span>

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

### <span data-ttu-id="fafbf-121">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="fafbf-121">-CertificatePassword</span></span>
<span data-ttu-id="fafbf-122">인증서 파일의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="fafbf-122">The password of the certificate file.</span></span>

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

### <span data-ttu-id="fafbf-123">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="fafbf-123">-CertificateSubjectName</span></span>
<span data-ttu-id="fafbf-124">만들려는 인증서의 Dns 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fafbf-124">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="fafbf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fafbf-125">-DefaultProfile</span></span>
<span data-ttu-id="fafbf-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fafbf-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fafbf-127">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="fafbf-127">-KeyVaultName</span></span>
<span data-ttu-id="fafbf-128">Azure 키 보관소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fafbf-128">Azure key vault name.</span></span>

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

### <span data-ttu-id="fafbf-129">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="fafbf-129">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="fafbf-130">Azure 키 보관소 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fafbf-130">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="fafbf-131">-이름</span><span class="sxs-lookup"><span data-stu-id="fafbf-131">-Name</span></span>
<span data-ttu-id="fafbf-132">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fafbf-132">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="fafbf-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fafbf-133">-ResourceGroupName</span></span>
<span data-ttu-id="fafbf-134">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fafbf-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="fafbf-135">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="fafbf-135">-SecretIdentifier</span></span>
<span data-ttu-id="fafbf-136">기존 Azure 키 자격 증명 모음 비밀 Url입니다.</span><span class="sxs-lookup"><span data-stu-id="fafbf-136">The existing Azure key vault secret Url.</span></span>

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

### <span data-ttu-id="fafbf-137">-확인</span><span class="sxs-lookup"><span data-stu-id="fafbf-137">-Confirm</span></span>
<span data-ttu-id="fafbf-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fafbf-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fafbf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fafbf-139">-WhatIf</span></span>
<span data-ttu-id="fafbf-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fafbf-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fafbf-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fafbf-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fafbf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fafbf-142">CommonParameters</span></span>
<span data-ttu-id="fafbf-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fafbf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fafbf-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fafbf-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fafbf-145">입력</span><span class="sxs-lookup"><span data-stu-id="fafbf-145">INPUTS</span></span>

### <span data-ttu-id="fafbf-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fafbf-146">System.String</span></span>
<span data-ttu-id="fafbf-147">매개 변수: CertificateFile (ByValue), CertificateOutputFolder (ByValue), CertificateSubjectName (ByValue), KeyVaultName (ByValue), KeyVaultResouceGroupName (byvalue), SecretIdentifier (byvalue)</span><span class="sxs-lookup"><span data-stu-id="fafbf-147">Parameters: CertificateFile (ByValue), CertificateOutputFolder (ByValue), CertificateSubjectName (ByValue), KeyVaultName (ByValue), KeyVaultResouceGroupName (ByValue), SecretIdentifier (ByValue)</span></span>

### <span data-ttu-id="fafbf-148">System.webserver</span><span class="sxs-lookup"><span data-stu-id="fafbf-148">System.Security.SecureString</span></span>
<span data-ttu-id="fafbf-149">매개 변수: CertificatePassword (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fafbf-149">Parameters: CertificatePassword (ByValue)</span></span>

## <span data-ttu-id="fafbf-150">출력</span><span class="sxs-lookup"><span data-stu-id="fafbf-150">OUTPUTS</span></span>

### <span data-ttu-id="fafbf-151">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="fafbf-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="fafbf-152">상속자</span><span class="sxs-lookup"><span data-stu-id="fafbf-152">NOTES</span></span>

## <span data-ttu-id="fafbf-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fafbf-153">RELATED LINKS</span></span>

[<span data-ttu-id="fafbf-154">제거-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="fafbf-154">Remove-AzureRmServiceFabricClusterCertificate</span></span>](./Remove-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="fafbf-155">새로운 AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="fafbf-155">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)

[<span data-ttu-id="fafbf-156">추가-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="fafbf-156">Add-AzureRmServiceFabricApplicationCertificate</span></span>](./Add-AzureRmServiceFabricApplicationCertificate.md)
