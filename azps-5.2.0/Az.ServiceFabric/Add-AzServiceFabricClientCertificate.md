---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: ca9dbbba29e6f770b727e1f96717c2626f112839
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369041"
---
# <span data-ttu-id="df4b8-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="df4b8-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="df4b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df4b8-102">SYNOPSIS</span></span>
<span data-ttu-id="df4b8-103">클라이언트 인증을 위해 클러스터에 일반 이름 또는 지문을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="df4b8-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="df4b8-104">구문</span><span class="sxs-lookup"><span data-stu-id="df4b8-104">SYNTAX</span></span>

### <span data-ttu-id="df4b8-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="df4b8-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df4b8-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="df4b8-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df4b8-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="df4b8-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df4b8-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="df4b8-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df4b8-109">설명</span><span class="sxs-lookup"><span data-stu-id="df4b8-109">DESCRIPTION</span></span>
<span data-ttu-id="df4b8-110">**Add-AzServiceFabricClientCertificate를** 사용하여 클러스터에 일반 이름 및 발급자 지문 또는 인증서 지문을 추가하여 클라이언트가 인증에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df4b8-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="df4b8-111">예제</span><span class="sxs-lookup"><span data-stu-id="df4b8-111">EXAMPLES</span></span>

### <span data-ttu-id="df4b8-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="df4b8-112">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="df4b8-113">이 명령은 지문 '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A'가 있는 인증서를 클러스터에 추가합니다. 따라서 클라이언트는 인증서를 관리자로 사용하여 클러스터와 통신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df4b8-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="df4b8-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="df4b8-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="df4b8-115">이 명령은 일반 이름이 'Contoso.com'이고 발급자 지문이 '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A'인 읽기 전용 클라이언트 인증서를 클러스터에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="df4b8-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="df4b8-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df4b8-116">PARAMETERS</span></span>

### <span data-ttu-id="df4b8-117">-Admin</span><span class="sxs-lookup"><span data-stu-id="df4b8-117">-Admin</span></span>
<span data-ttu-id="df4b8-118">클라이언트 인증 유형</span><span class="sxs-lookup"><span data-stu-id="df4b8-118">Client authentication type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df4b8-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="df4b8-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="df4b8-120">관리자 권한만 있는 클라이언트 인증서 지문 지정</span><span class="sxs-lookup"><span data-stu-id="df4b8-120">Specify client certificate thumbprint which only has admin permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df4b8-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="df4b8-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="df4b8-122">클라이언트 일반 이름, 발급자 지문 및 인증 유형 지정</span><span class="sxs-lookup"><span data-stu-id="df4b8-122">Specify client common name , issuer thumbprint and authentication type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df4b8-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="df4b8-123">-CommonName</span></span>
<span data-ttu-id="df4b8-124">클라이언트 인증서 일반 이름 지정</span><span class="sxs-lookup"><span data-stu-id="df4b8-124">Specify client certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df4b8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df4b8-125">-DefaultProfile</span></span>
<span data-ttu-id="df4b8-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="df4b8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df4b8-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="df4b8-127">-IssuerThumbprint</span></span>
<span data-ttu-id="df4b8-128">클라이언트 인증서 발급자 지문 지정</span><span class="sxs-lookup"><span data-stu-id="df4b8-128">Specify thumbprint of client certificate's issuer</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df4b8-129">-Name</span><span class="sxs-lookup"><span data-stu-id="df4b8-129">-Name</span></span>
<span data-ttu-id="df4b8-130">클러스터의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="df4b8-130">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="df4b8-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="df4b8-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="df4b8-132">읽기 전용 권한만 있는 클라이언트 인증서 지문 지정</span><span class="sxs-lookup"><span data-stu-id="df4b8-132">Specify client certificate thumbprint which only has read only permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df4b8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df4b8-133">-ResourceGroupName</span></span>
<span data-ttu-id="df4b8-134">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df4b8-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="df4b8-135">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="df4b8-135">-Thumbprint</span></span>
<span data-ttu-id="df4b8-136">클라이언트 인증서 지문 지정</span><span class="sxs-lookup"><span data-stu-id="df4b8-136">Specify client certificate thumbprint</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df4b8-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df4b8-137">-Confirm</span></span>
<span data-ttu-id="df4b8-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="df4b8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df4b8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df4b8-139">-WhatIf</span></span>
<span data-ttu-id="df4b8-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="df4b8-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df4b8-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df4b8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df4b8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df4b8-142">CommonParameters</span></span>
<span data-ttu-id="df4b8-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="df4b8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df4b8-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="df4b8-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df4b8-145">입력</span><span class="sxs-lookup"><span data-stu-id="df4b8-145">INPUTS</span></span>

### <span data-ttu-id="df4b8-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="df4b8-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="df4b8-147">System.String</span><span class="sxs-lookup"><span data-stu-id="df4b8-147">System.String</span></span>

### <span data-ttu-id="df4b8-148">System.String[]</span><span class="sxs-lookup"><span data-stu-id="df4b8-148">System.String[]</span></span>

### <span data-ttu-id="df4b8-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span><span class="sxs-lookup"><span data-stu-id="df4b8-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="df4b8-150">출력</span><span class="sxs-lookup"><span data-stu-id="df4b8-150">OUTPUTS</span></span>

### <span data-ttu-id="df4b8-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="df4b8-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="df4b8-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="df4b8-152">NOTES</span></span>

## <span data-ttu-id="df4b8-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df4b8-153">RELATED LINKS</span></span>

[<span data-ttu-id="df4b8-154">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="df4b8-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)
