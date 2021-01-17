---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
ms.openlocfilehash: 36ed679066d1850851ff0e90f39eb6f9ef8ffa1a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348626"
---
# <span data-ttu-id="4bb44-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="4bb44-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>

## <span data-ttu-id="4bb44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bb44-102">SYNOPSIS</span></span>
<span data-ttu-id="4bb44-103">노드 형식에 인증서 비밀을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb44-103">Add certificate secret to the node type.</span></span>

## <span data-ttu-id="4bb44-104">구문</span><span class="sxs-lookup"><span data-stu-id="4bb44-104">SYNTAX</span></span>

### <span data-ttu-id="4bb44-105">ByObj(기본값)</span><span class="sxs-lookup"><span data-stu-id="4bb44-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-InputObject] <PSManagedNodeType> -SourceVaultId <String>
 -CertificateUrl <String> -CertificateStore <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bb44-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4bb44-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> -SourceVaultId <String> -CertificateUrl <String> -CertificateStore <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bb44-107">설명</span><span class="sxs-lookup"><span data-stu-id="4bb44-107">DESCRIPTION</span></span>
<span data-ttu-id="4bb44-108">노드 형식에 인증서 비밀을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb44-108">Add certificate secret to the node type.</span></span> <span data-ttu-id="4bb44-109">비밀은 Azure Key Vault에 저장되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb44-109">The secret must be stored in an Azure Key Vault.</span></span> <span data-ttu-id="4bb44-110">Key Vault와 관련된 자세한 내용은 Azure Key Vault란?</span><span class="sxs-lookup"><span data-stu-id="4bb44-110">For more information relating to Key Vault, see What is Azure Key Vault?</span></span> <span data-ttu-id="4bb44-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="4bb44-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span> <span data-ttu-id="4bb44-112">cmdlet에 대한 자세한 내용은 Azure Key Vault cmdlet(Microsoft Developer Network 라이브러리 또는 Set-AzKeyVaultSecret https://msdn.microsoft.com/library/azure/dn868052.aspx) cmdlet)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4bb44-112">For more information about the cmdlets, see Azure Key Vault Cmdlets (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the Set-AzKeyVaultSecret cmdlet.</span></span>

## <span data-ttu-id="4bb44-113">예제</span><span class="sxs-lookup"><span data-stu-id="4bb44-113">EXAMPLES</span></span>

### <span data-ttu-id="4bb44-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="4bb44-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Add-AzServiceFabricManagedNodeTypeVMSecret -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="4bb44-115">이 콤마는 지정된 키 자격 증명 및 비밀 식별자에서 인증서 비밀을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb44-115">This commad adds a certificate secret from the keyvault and secret identifier specified.</span></span>

### <span data-ttu-id="4bb44-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="4bb44-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMSecret -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="4bb44-117">이 콤마는 파이핑을 통해 지정된 키 자격 증명 및 비밀 식별자에서 인증서 비밀을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb44-117">This commad adds a certificate secret from the keyvault and secret identifier specified, with piping.</span></span>

## <span data-ttu-id="4bb44-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bb44-118">PARAMETERS</span></span>

### <span data-ttu-id="4bb44-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bb44-119">-AsJob</span></span>
<span data-ttu-id="4bb44-120">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb44-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4bb44-121">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="4bb44-121">-CertificateStore</span></span>
<span data-ttu-id="4bb44-122">인증서를 추가할 Virtual Machine의 인증서 저장소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb44-122">Specifies the certificate store on the Virtual Machine to which the certificate should be added.</span></span>
<span data-ttu-id="4bb44-123">지정된 인증서 저장소는 LocalMachine 계정에 암시적으로 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bb44-123">The specified certificate store is implicitly in the LocalMachine account.</span></span>

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

### <span data-ttu-id="4bb44-124">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="4bb44-124">-CertificateUrl</span></span>
<span data-ttu-id="4bb44-125">Key Vault에 비밀로 업로드된 인증서의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="4bb44-125">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
<span data-ttu-id="4bb44-126">Key Vault에 비밀을 추가하는 내용은 키 자격 증명 모음에 키 또는 비밀 \[ \] https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add) 추가(.</span><span class="sxs-lookup"><span data-stu-id="4bb44-126">For adding a secret to the Key Vault, see \[Add a key or secret to the key vault\](https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add).</span></span>
<span data-ttu-id="4bb44-127">이 경우 인증서는 UTF-8로 인코딩된 다음 JSON 개체의 Base64 인코딩입니다. \<br\> \<br\> { \<br\> "data":" \<Base64-encoded-certificate\> ", \<br\> "dataType":"pfx", \<br\> "password":" \<pfx-file-password\> " \<br\> }/</span><span class="sxs-lookup"><span data-stu-id="4bb44-127">In this case, your certificate needs to be It is the Base64 encoding of the following JSON Object which is encoded in UTF-8: \<br\>\<br\> {\<br\>  "data":"\<Base64-encoded-certificate\>",\<br\>  "dataType":"pfx",\<br\>  "password":"\<pfx-file-password\>"\<br\>}/</span></span>

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

### <span data-ttu-id="4bb44-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4bb44-128">-ClusterName</span></span>
<span data-ttu-id="4bb44-129">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb44-129">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="4bb44-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bb44-130">-DefaultProfile</span></span>
<span data-ttu-id="4bb44-131">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4bb44-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bb44-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bb44-132">-InputObject</span></span>
<span data-ttu-id="4bb44-133">노드 유형 리소스</span><span class="sxs-lookup"><span data-stu-id="4bb44-133">Node Type resource</span></span>

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

### <span data-ttu-id="4bb44-134">-Name</span><span class="sxs-lookup"><span data-stu-id="4bb44-134">-Name</span></span>
<span data-ttu-id="4bb44-135">노드 형식의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb44-135">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="4bb44-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bb44-136">-ResourceGroupName</span></span>
<span data-ttu-id="4bb44-137">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb44-137">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="4bb44-138">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="4bb44-138">-SourceVaultId</span></span>
<span data-ttu-id="4bb44-139">인증서를 포함하는 Key Vault 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4bb44-139">Key Vault resource id containing the certificates.</span></span>

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

### <span data-ttu-id="4bb44-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4bb44-140">-Confirm</span></span>
<span data-ttu-id="4bb44-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bb44-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bb44-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bb44-142">-WhatIf</span></span>
<span data-ttu-id="4bb44-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4bb44-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bb44-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4bb44-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bb44-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bb44-145">CommonParameters</span></span>
<span data-ttu-id="4bb44-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb44-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bb44-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4bb44-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bb44-148">입력</span><span class="sxs-lookup"><span data-stu-id="4bb44-148">INPUTS</span></span>

### <span data-ttu-id="4bb44-149">System.String</span><span class="sxs-lookup"><span data-stu-id="4bb44-149">System.String</span></span>

## <span data-ttu-id="4bb44-150">출력</span><span class="sxs-lookup"><span data-stu-id="4bb44-150">OUTPUTS</span></span>

### <span data-ttu-id="4bb44-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="4bb44-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="4bb44-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4bb44-152">NOTES</span></span>

## <span data-ttu-id="4bb44-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4bb44-153">RELATED LINKS</span></span>
