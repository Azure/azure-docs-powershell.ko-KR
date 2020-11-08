---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
ms.openlocfilehash: 36ed679066d1850851ff0e90f39eb6f9ef8ffa1a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048739"
---
# <span data-ttu-id="58471-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="58471-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>

## <span data-ttu-id="58471-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58471-102">SYNOPSIS</span></span>
<span data-ttu-id="58471-103">노드 형식에 인증서 비밀을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="58471-103">Add certificate secret to the node type.</span></span>

## <span data-ttu-id="58471-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58471-104">SYNTAX</span></span>

### <span data-ttu-id="58471-105">ByObj (기본값)</span><span class="sxs-lookup"><span data-stu-id="58471-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-InputObject] <PSManagedNodeType> -SourceVaultId <String>
 -CertificateUrl <String> -CertificateStore <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58471-106">ByName</span><span class="sxs-lookup"><span data-stu-id="58471-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> -SourceVaultId <String> -CertificateUrl <String> -CertificateStore <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58471-107">설명은</span><span class="sxs-lookup"><span data-stu-id="58471-107">DESCRIPTION</span></span>
<span data-ttu-id="58471-108">노드 형식에 인증서 비밀을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="58471-108">Add certificate secret to the node type.</span></span> <span data-ttu-id="58471-109">비밀은 Azure Key Vault에 저장 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58471-109">The secret must be stored in an Azure Key Vault.</span></span> <span data-ttu-id="58471-110">키 볼트에 대 한 자세한 내용은 Azure 키 보관소 란?을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="58471-110">For more information relating to Key Vault, see What is Azure Key Vault?</span></span> <span data-ttu-id="58471-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="58471-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span> <span data-ttu-id="58471-112">Cmdlet에 대 한 자세한 내용은 Azure 키 자격 증명 모음 Cmdlet ( https://msdn.microsoft.com/library/azure/dn868052.aspx) Microsoft 개발자 네트워크 라이브러리 또는 Set-AzKeyVaultSecret cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="58471-112">For more information about the cmdlets, see Azure Key Vault Cmdlets (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the Set-AzKeyVaultSecret cmdlet.</span></span>

## <span data-ttu-id="58471-113">예제의</span><span class="sxs-lookup"><span data-stu-id="58471-113">EXAMPLES</span></span>

### <span data-ttu-id="58471-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="58471-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Add-AzServiceFabricManagedNodeTypeVMSecret -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="58471-115">이 commad는 지정 된 keyvault 및 비밀 id의 인증서 비밀을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="58471-115">This commad adds a certificate secret from the keyvault and secret identifier specified.</span></span>

### <span data-ttu-id="58471-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="58471-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMSecret -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="58471-117">이 commad는 지정 된 keyvault 및 비밀 식별자의 인증서 비밀을 파이핑을 사용 하 여 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="58471-117">This commad adds a certificate secret from the keyvault and secret identifier specified, with piping.</span></span>

## <span data-ttu-id="58471-118">변수</span><span class="sxs-lookup"><span data-stu-id="58471-118">PARAMETERS</span></span>

### <span data-ttu-id="58471-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58471-119">-AsJob</span></span>
<span data-ttu-id="58471-120">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="58471-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="58471-121">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="58471-121">-CertificateStore</span></span>
<span data-ttu-id="58471-122">인증서를 추가 해야 하는 가상 컴퓨터의 인증서 저장소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58471-122">Specifies the certificate store on the Virtual Machine to which the certificate should be added.</span></span>
<span data-ttu-id="58471-123">지정 된 인증서 저장소가 LocalMachine 계정에 암시적으로 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58471-123">The specified certificate store is implicitly in the LocalMachine account.</span></span>

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

### <span data-ttu-id="58471-124">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="58471-124">-CertificateUrl</span></span>
<span data-ttu-id="58471-125">키 자격 증명 모음에 비밀으로 업로드 된 인증서의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="58471-125">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
<span data-ttu-id="58471-126">키 자격 증명 모음에 비밀을 추가 하려면 키 \[ 자격 증명 모음에 키 또는 비밀 추가 (을 (를) 참조 하세요 \] https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add) .</span><span class="sxs-lookup"><span data-stu-id="58471-126">For adding a secret to the Key Vault, see \[Add a key or secret to the key vault\](https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add).</span></span>
<span data-ttu-id="58471-127">이 경우 인증서는 u t f-8로 인코딩된 다음 JSON 개체의 Base64 인코딩 ( \<br\> \<br\> { \<br\> "data": " \<Base64-encoded-certificate\> ", \<br\> "dataType": "pfx", \<br\> "password": " \<pfx-file-password\> ") \<br\> 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58471-127">In this case, your certificate needs to be It is the Base64 encoding of the following JSON Object which is encoded in UTF-8: \<br\>\<br\> {\<br\>  "data":"\<Base64-encoded-certificate\>",\<br\>  "dataType":"pfx",\<br\>  "password":"\<pfx-file-password\>"\<br\>}/</span></span>

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

### <span data-ttu-id="58471-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="58471-128">-ClusterName</span></span>
<span data-ttu-id="58471-129">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58471-129">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="58471-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58471-130">-DefaultProfile</span></span>
<span data-ttu-id="58471-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58471-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58471-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58471-132">-InputObject</span></span>
<span data-ttu-id="58471-133">노드 형식 리소스</span><span class="sxs-lookup"><span data-stu-id="58471-133">Node Type resource</span></span>

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

### <span data-ttu-id="58471-134">-이름</span><span class="sxs-lookup"><span data-stu-id="58471-134">-Name</span></span>
<span data-ttu-id="58471-135">노드 형식의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58471-135">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="58471-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58471-136">-ResourceGroupName</span></span>
<span data-ttu-id="58471-137">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58471-137">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="58471-138">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="58471-138">-SourceVaultId</span></span>
<span data-ttu-id="58471-139">인증서를 포함 하는 키 자격 증명 모음 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="58471-139">Key Vault resource id containing the certificates.</span></span>

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

### <span data-ttu-id="58471-140">-확인</span><span class="sxs-lookup"><span data-stu-id="58471-140">-Confirm</span></span>
<span data-ttu-id="58471-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="58471-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58471-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58471-142">-WhatIf</span></span>
<span data-ttu-id="58471-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="58471-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58471-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58471-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58471-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58471-145">CommonParameters</span></span>
<span data-ttu-id="58471-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58471-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58471-147">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="58471-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58471-148">입력</span><span class="sxs-lookup"><span data-stu-id="58471-148">INPUTS</span></span>

### <span data-ttu-id="58471-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="58471-149">System.String</span></span>

## <span data-ttu-id="58471-150">출력</span><span class="sxs-lookup"><span data-stu-id="58471-150">OUTPUTS</span></span>

### <span data-ttu-id="58471-151">ServiceFabric. a i m.</span><span class="sxs-lookup"><span data-stu-id="58471-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="58471-152">상속자</span><span class="sxs-lookup"><span data-stu-id="58471-152">NOTES</span></span>

## <span data-ttu-id="58471-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58471-153">RELATED LINKS</span></span>
