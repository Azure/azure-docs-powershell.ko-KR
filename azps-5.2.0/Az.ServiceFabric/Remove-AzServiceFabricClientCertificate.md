---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: c7a88cad933781b00e720c273be467966991cebf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341558"
---
# <span data-ttu-id="3cfa8-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3cfa8-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="3cfa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cfa8-102">SYNOPSIS</span></span>
<span data-ttu-id="3cfa8-103">클러스터에 대한 클라이언트 인증에 사용되는 클라이언트 인증서 또는 인증서 주체 이름을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3cfa8-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="3cfa8-104">구문</span><span class="sxs-lookup"><span data-stu-id="3cfa8-104">SYNTAX</span></span>

### <span data-ttu-id="3cfa8-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="3cfa8-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cfa8-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="3cfa8-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cfa8-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="3cfa8-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cfa8-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="3cfa8-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cfa8-109">설명</span><span class="sxs-lookup"><span data-stu-id="3cfa8-109">DESCRIPTION</span></span>
<span data-ttu-id="3cfa8-110">**Remove-AzServiceFabricClientCertificate를** 사용하여 클러스터에 대한 클라이언트 인증에 사용되는 클라이언트 인증서 또는 인증서 주체 이름을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3cfa8-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="3cfa8-111">예제</span><span class="sxs-lookup"><span data-stu-id="3cfa8-111">EXAMPLES</span></span>

### <span data-ttu-id="3cfa8-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="3cfa8-112">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="3cfa8-113">이 명령은 클러스터에서 지문 '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A'가 있는 클라이언트 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3cfa8-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="3cfa8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cfa8-114">PARAMETERS</span></span>

### <span data-ttu-id="3cfa8-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="3cfa8-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="3cfa8-116">관리자 권한만 있는 클라이언트 인증서 지문 지정</span><span class="sxs-lookup"><span data-stu-id="3cfa8-116">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="3cfa8-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="3cfa8-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="3cfa8-118">클라이언트 일반 이름, 발급자 지문 및 인증 유형 지정</span><span class="sxs-lookup"><span data-stu-id="3cfa8-118">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="3cfa8-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="3cfa8-119">-CommonName</span></span>
<span data-ttu-id="3cfa8-120">클라이언트 인증서 일반 이름 지정</span><span class="sxs-lookup"><span data-stu-id="3cfa8-120">Specify client certificate common name</span></span>

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

### <span data-ttu-id="3cfa8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cfa8-121">-DefaultProfile</span></span>
<span data-ttu-id="3cfa8-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3cfa8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cfa8-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="3cfa8-123">-IssuerThumbprint</span></span>
<span data-ttu-id="3cfa8-124">클라이언트 인증서 발급자 지문 지정</span><span class="sxs-lookup"><span data-stu-id="3cfa8-124">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="3cfa8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="3cfa8-125">-Name</span></span>
<span data-ttu-id="3cfa8-126">클러스터의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="3cfa8-126">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="3cfa8-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="3cfa8-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="3cfa8-128">읽기 전용 권한만 있는 클라이언트 인증서 지문 지정</span><span class="sxs-lookup"><span data-stu-id="3cfa8-128">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="3cfa8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cfa8-129">-ResourceGroupName</span></span>
<span data-ttu-id="3cfa8-130">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3cfa8-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="3cfa8-131">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="3cfa8-131">-Thumbprint</span></span>
<span data-ttu-id="3cfa8-132">클라이언트 인증서 지문 지정</span><span class="sxs-lookup"><span data-stu-id="3cfa8-132">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="3cfa8-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3cfa8-133">-Confirm</span></span>
<span data-ttu-id="3cfa8-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cfa8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cfa8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cfa8-135">-WhatIf</span></span>
<span data-ttu-id="3cfa8-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3cfa8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cfa8-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3cfa8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cfa8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cfa8-138">CommonParameters</span></span>
<span data-ttu-id="3cfa8-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3cfa8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cfa8-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3cfa8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cfa8-141">입력</span><span class="sxs-lookup"><span data-stu-id="3cfa8-141">INPUTS</span></span>

### <span data-ttu-id="3cfa8-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3cfa8-142">System.String</span></span>

### <span data-ttu-id="3cfa8-143">System.String[]</span><span class="sxs-lookup"><span data-stu-id="3cfa8-143">System.String[]</span></span>

### <span data-ttu-id="3cfa8-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span><span class="sxs-lookup"><span data-stu-id="3cfa8-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="3cfa8-145">출력</span><span class="sxs-lookup"><span data-stu-id="3cfa8-145">OUTPUTS</span></span>

### <span data-ttu-id="3cfa8-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="3cfa8-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="3cfa8-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3cfa8-147">NOTES</span></span>

## <span data-ttu-id="3cfa8-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3cfa8-148">RELATED LINKS</span></span>

[<span data-ttu-id="3cfa8-149">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3cfa8-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)