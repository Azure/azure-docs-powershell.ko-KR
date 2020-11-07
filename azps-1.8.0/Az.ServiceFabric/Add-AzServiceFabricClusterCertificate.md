---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: bf96b4a21e12e41ce067d669b50c05831a162a8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699125"
---
# <span data-ttu-id="42dc2-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="42dc2-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="42dc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="42dc2-103">클러스터에 보조 클러스터 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="42dc2-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="42dc2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="42dc2-104">SYNTAX</span></span>

### <span data-ttu-id="42dc2-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="42dc2-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42dc2-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="42dc2-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42dc2-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="42dc2-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42dc2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="42dc2-108">DESCRIPTION</span></span>
<span data-ttu-id="42dc2-109">**추가-AzServiceFabricClusterCertificate** 를 사용 하 여 기존 azure 키 자격 증명 모음에서 보조 클러스터 인증서를 추가 하거나 제공 된 기존 인증서를 사용 하 여 새 azure 키 자격 증명 모음을 만들거나, 만든 새 인증서에서 생성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="42dc2-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="42dc2-110">보조 클러스터가 있으면이를 재정의 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42dc2-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="42dc2-111">예제의</span><span class="sxs-lookup"><span data-stu-id="42dc2-111">EXAMPLES</span></span>

### <span data-ttu-id="42dc2-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="42dc2-112">Example 1</span></span>
```
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="42dc2-113">이 명령은 기존 Azure key 자격 증명 모음에 보조 클러스터 인증서로 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="42dc2-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="42dc2-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="42dc2-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="42dc2-115">이 명령은 Azure key vault에 자체 서명 된 인증서를 만들고 보조 클러스터 인증서로 사용 하도록 클러스터를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="42dc2-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="42dc2-116">변수</span><span class="sxs-lookup"><span data-stu-id="42dc2-116">PARAMETERS</span></span>

### <span data-ttu-id="42dc2-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="42dc2-117">-CertificateCommonName</span></span>
<span data-ttu-id="42dc2-118">인증서 일반 이름</span><span class="sxs-lookup"><span data-stu-id="42dc2-118">Certificate common name</span></span>

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

### <span data-ttu-id="42dc2-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="42dc2-119">-CertificateFile</span></span>
<span data-ttu-id="42dc2-120">기존 인증서 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="42dc2-120">The existing certificate file path.</span></span>

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

### <span data-ttu-id="42dc2-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="42dc2-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="42dc2-122">인증서 발급자 지문 (두 개 이상 있는 경우 쉼표로 구분)</span><span class="sxs-lookup"><span data-stu-id="42dc2-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="42dc2-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="42dc2-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="42dc2-124">만들려는 새 인증서의 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="42dc2-124">The folder of the new certificate to be created.</span></span>

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

### <span data-ttu-id="42dc2-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="42dc2-125">-CertificatePassword</span></span>
<span data-ttu-id="42dc2-126">인증서 파일의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="42dc2-126">The password of the certificate file.</span></span>

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

### <span data-ttu-id="42dc2-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="42dc2-127">-CertificateSubjectName</span></span>
<span data-ttu-id="42dc2-128">만들려는 인증서의 Dns 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42dc2-128">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="42dc2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42dc2-129">-DefaultProfile</span></span>
<span data-ttu-id="42dc2-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42dc2-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42dc2-131">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="42dc2-131">-KeyVaultName</span></span>
<span data-ttu-id="42dc2-132">Azure 키 보관소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42dc2-132">Azure key vault name.</span></span>

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

### <span data-ttu-id="42dc2-133">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="42dc2-133">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="42dc2-134">Azure 키 보관소 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42dc2-134">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="42dc2-135">-이름</span><span class="sxs-lookup"><span data-stu-id="42dc2-135">-Name</span></span>
<span data-ttu-id="42dc2-136">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42dc2-136">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="42dc2-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42dc2-137">-ResourceGroupName</span></span>
<span data-ttu-id="42dc2-138">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42dc2-138">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="42dc2-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="42dc2-139">-SecretIdentifier</span></span>
<span data-ttu-id="42dc2-140">기존 Azure 키 자격 증명 모음 비밀 Url입니다.</span><span class="sxs-lookup"><span data-stu-id="42dc2-140">The existing Azure key vault secret Url.</span></span>

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

### <span data-ttu-id="42dc2-141">-확인</span><span class="sxs-lookup"><span data-stu-id="42dc2-141">-Confirm</span></span>
<span data-ttu-id="42dc2-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="42dc2-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42dc2-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42dc2-143">-WhatIf</span></span>
<span data-ttu-id="42dc2-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="42dc2-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42dc2-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42dc2-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42dc2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42dc2-146">CommonParameters</span></span>
<span data-ttu-id="42dc2-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="42dc2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42dc2-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42dc2-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42dc2-149">입력</span><span class="sxs-lookup"><span data-stu-id="42dc2-149">INPUTS</span></span>

### <span data-ttu-id="42dc2-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="42dc2-150">System.String</span></span>

### <span data-ttu-id="42dc2-151">System.webserver</span><span class="sxs-lookup"><span data-stu-id="42dc2-151">System.Security.SecureString</span></span>

## <span data-ttu-id="42dc2-152">출력</span><span class="sxs-lookup"><span data-stu-id="42dc2-152">OUTPUTS</span></span>

### <span data-ttu-id="42dc2-153">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="42dc2-153">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="42dc2-154">상속자</span><span class="sxs-lookup"><span data-stu-id="42dc2-154">NOTES</span></span>

## <span data-ttu-id="42dc2-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42dc2-155">RELATED LINKS</span></span>

[<span data-ttu-id="42dc2-156">제거-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="42dc2-156">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="42dc2-157">새로운 AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="42dc2-157">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)

[<span data-ttu-id="42dc2-158">추가-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="42dc2-158">Add-AzServiceFabricApplicationCertificate</span></span>](./Add-AzServiceFabricApplicationCertificate.md)
