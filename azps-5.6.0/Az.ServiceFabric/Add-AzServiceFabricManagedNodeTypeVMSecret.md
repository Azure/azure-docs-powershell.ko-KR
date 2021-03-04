---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
ms.openlocfilehash: 35d755bc117ccc4379be8d7344d8e7170594d555
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969792"
---
# <span data-ttu-id="464ef-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="464ef-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>

## <span data-ttu-id="464ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="464ef-102">SYNOPSIS</span></span>
<span data-ttu-id="464ef-103">노드 유형에 인증서 비밀을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="464ef-103">Add certificate secret to the node type.</span></span>

## <span data-ttu-id="464ef-104">구문</span><span class="sxs-lookup"><span data-stu-id="464ef-104">SYNTAX</span></span>

### <span data-ttu-id="464ef-105">ByObj(기본값)</span><span class="sxs-lookup"><span data-stu-id="464ef-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-InputObject] <PSManagedNodeType> -SourceVaultId <String>
 -CertificateUrl <String> -CertificateStore <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="464ef-106">ByName</span><span class="sxs-lookup"><span data-stu-id="464ef-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> -SourceVaultId <String> -CertificateUrl <String> -CertificateStore <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="464ef-107">설명</span><span class="sxs-lookup"><span data-stu-id="464ef-107">DESCRIPTION</span></span>
<span data-ttu-id="464ef-108">노드 유형에 인증서 비밀을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="464ef-108">Add certificate secret to the node type.</span></span> <span data-ttu-id="464ef-109">비밀은 Azure Key Vault에 저장되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="464ef-109">The secret must be stored in an Azure Key Vault.</span></span> <span data-ttu-id="464ef-110">Key Vault와 관련된 자세한 내용은 Azure Key Vault란?</span><span class="sxs-lookup"><span data-stu-id="464ef-110">For more information relating to Key Vault, see What is Azure Key Vault?</span></span> <span data-ttu-id="464ef-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="464ef-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span> <span data-ttu-id="464ef-112">cmdlet에 대한 자세한 내용은 Azure Key Vault cmdlet(Microsoft Developer Network 라이브러리 또는 Set-AzKeyVaultSecret https://msdn.microsoft.com/library/azure/dn868052.aspx) cmdlet)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="464ef-112">For more information about the cmdlets, see Azure Key Vault Cmdlets (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the Set-AzKeyVaultSecret cmdlet.</span></span>

## <span data-ttu-id="464ef-113">예제</span><span class="sxs-lookup"><span data-stu-id="464ef-113">EXAMPLES</span></span>

### <span data-ttu-id="464ef-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="464ef-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Add-AzServiceFabricManagedNodeTypeVMSecret -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="464ef-115">이 콤마는 지정된 keyvault 및 비밀 식별자에서 인증서 비밀을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="464ef-115">This commad adds a certificate secret from the keyvault and secret identifier specified.</span></span>

### <span data-ttu-id="464ef-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="464ef-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMSecret -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="464ef-117">이 콤마는 배관과 함께 지정된 keyvault 및 비밀 식별자에서 인증서 비밀을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="464ef-117">This commad adds a certificate secret from the keyvault and secret identifier specified, with piping.</span></span>

## <span data-ttu-id="464ef-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="464ef-118">PARAMETERS</span></span>

### <span data-ttu-id="464ef-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="464ef-119">-AsJob</span></span>
<span data-ttu-id="464ef-120">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="464ef-120">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="464ef-121">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="464ef-121">-CertificateStore</span></span>
<span data-ttu-id="464ef-122">인증서를 추가해야 하는 Virtual Machine에 인증서 저장소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="464ef-122">Specifies the certificate store on the Virtual Machine to which the certificate should be added.</span></span>
<span data-ttu-id="464ef-123">지정된 인증서 저장소는 LocalMachine 계정에 암시적으로 있습니다.</span><span class="sxs-lookup"><span data-stu-id="464ef-123">The specified certificate store is implicitly in the LocalMachine account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="464ef-124">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="464ef-124">-CertificateUrl</span></span>
<span data-ttu-id="464ef-125">Key Vault에 비밀로 업로드된 인증서의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="464ef-125">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
<span data-ttu-id="464ef-126">Key Vault에 비밀을 추가하는 경우 키 자격 증명 모음에 키 또는 비밀 추가를 \[ \] https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add) 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="464ef-126">For adding a secret to the Key Vault, see \[Add a key or secret to the key vault\](https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add).</span></span>
<span data-ttu-id="464ef-127">이 경우 인증서는 UTF-8: \<br\> \<br\> \<br\> {"data":", \<Base64-encoded-certificate\> \<br\> "dataType":"pfx", \<br\> "password":" \<pfx-file-password\> \<br\> "}/으로 인코딩된 다음 JSON 개체의 Base64 인코딩입니다.</span><span class="sxs-lookup"><span data-stu-id="464ef-127">In this case, your certificate needs to be It is the Base64 encoding of the following JSON Object which is encoded in UTF-8: \<br\>\<br\> {\<br\>  "data":"\<Base64-encoded-certificate\>",\<br\>  "dataType":"pfx",\<br\>  "password":"\<pfx-file-password\>"\<br\>}/</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="464ef-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="464ef-128">-ClusterName</span></span>
<span data-ttu-id="464ef-129">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="464ef-129">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="464ef-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="464ef-130">-DefaultProfile</span></span>
<span data-ttu-id="464ef-131">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="464ef-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="464ef-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="464ef-132">-InputObject</span></span>
<span data-ttu-id="464ef-133">노드 유형 리소스</span><span class="sxs-lookup"><span data-stu-id="464ef-133">Node Type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="464ef-134">-Name</span><span class="sxs-lookup"><span data-stu-id="464ef-134">-Name</span></span>
<span data-ttu-id="464ef-135">노드 형식의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="464ef-135">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="464ef-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="464ef-136">-ResourceGroupName</span></span>
<span data-ttu-id="464ef-137">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="464ef-137">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="464ef-138">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="464ef-138">-SourceVaultId</span></span>
<span data-ttu-id="464ef-139">인증서를 포함하는 Key Vault 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="464ef-139">Key Vault resource id containing the certificates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="464ef-140">-확인</span><span class="sxs-lookup"><span data-stu-id="464ef-140">-Confirm</span></span>
<span data-ttu-id="464ef-141">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="464ef-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="464ef-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="464ef-142">-WhatIf</span></span>
<span data-ttu-id="464ef-143">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="464ef-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="464ef-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="464ef-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="464ef-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="464ef-145">CommonParameters</span></span>
<span data-ttu-id="464ef-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="464ef-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="464ef-147">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="464ef-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="464ef-148">입력</span><span class="sxs-lookup"><span data-stu-id="464ef-148">INPUTS</span></span>

### <span data-ttu-id="464ef-149">System.String</span><span class="sxs-lookup"><span data-stu-id="464ef-149">System.String</span></span>

## <span data-ttu-id="464ef-150">출력</span><span class="sxs-lookup"><span data-stu-id="464ef-150">OUTPUTS</span></span>

### <span data-ttu-id="464ef-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="464ef-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="464ef-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="464ef-152">NOTES</span></span>

## <span data-ttu-id="464ef-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="464ef-153">RELATED LINKS</span></span>
