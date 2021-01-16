---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 1183a2aa6bf452d77ebe3975024067244075e5fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374256"
---
# <span data-ttu-id="a0156-101">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="a0156-101">Test-AzStackHCIConnection</span></span>

## <span data-ttu-id="a0156-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0156-102">SYNOPSIS</span></span>
<span data-ttu-id="a0156-103">Test-AzStackHCIConnection 클러스터형 노드에서 Azure Stack HCI에 필요한 Azure 서비스로의 연결을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0156-103">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="a0156-104">구문</span><span class="sxs-lookup"><span data-stu-id="a0156-104">SYNTAX</span></span>

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="a0156-105">설명</span><span class="sxs-lookup"><span data-stu-id="a0156-105">DESCRIPTION</span></span>
<span data-ttu-id="a0156-106">Test-AzStackHCIConnection 클러스터형 노드에서 Azure Stack HCI에 필요한 Azure 서비스로의 연결을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0156-106">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="a0156-107">예제</span><span class="sxs-lookup"><span data-stu-id="a0156-107">EXAMPLES</span></span>

### <span data-ttu-id="a0156-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a0156-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node. Success case.
```

<span data-ttu-id="a0156-109">C:\PS \> Test-AzStackHCIConnection 테스트: Azure Stack HCI 서비스 EndpointTested에 연결: https://azurestackhci-df.azurefd.net/health IsRequired: True 결과: 성공</span><span class="sxs-lookup"><span data-stu-id="a0156-109">C:\PS\>Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Succeeded</span></span>

### <span data-ttu-id="a0156-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="a0156-110">EXAMPLE 2</span></span>
```
Invoking on one of the cluster node. Failed case.
```

<span data-ttu-id="a0156-111">C:\PS \> Test-AzStackHCIConnection 테스트: Azure Stack HCI 서비스 EndpointTested에 연결: https://azurestackhci-df.azurefd.net/health IsRequired: True 결과: FailedNodes: Node1inClus2, Node2inClus3</span><span class="sxs-lookup"><span data-stu-id="a0156-111">C:\PS\>Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Failed FailedNodes: Node1inClus2, Node2inClus3</span></span>

## <span data-ttu-id="a0156-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0156-112">PARAMETERS</span></span>

### <span data-ttu-id="a0156-113">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="a0156-113">-ComputerName</span></span>
<span data-ttu-id="a0156-114">Azure에 등록되는 클러스터의 클러스터 노드 중 하나를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0156-114">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0156-115">-Credential</span><span class="sxs-lookup"><span data-stu-id="a0156-115">-Credential</span></span>
<span data-ttu-id="a0156-116">ComputerName의 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0156-116">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="a0156-117">기본값은 Cmdlet을 실행하는 현재 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="a0156-117">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0156-118">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="a0156-118">-EnvironmentName</span></span>
<span data-ttu-id="a0156-119">Azure 환경을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0156-119">Specifies the Azure Environment.</span></span>
<span data-ttu-id="a0156-120">기본값은 AzureCloud입니다.</span><span class="sxs-lookup"><span data-stu-id="a0156-120">Default is AzureCloud.</span></span>
<span data-ttu-id="a0156-121">유효한 값은 AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE입니다.</span><span class="sxs-lookup"><span data-stu-id="a0156-121">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0156-122">-Region</span><span class="sxs-lookup"><span data-stu-id="a0156-122">-Region</span></span>
<span data-ttu-id="a0156-123">연결할 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0156-123">Specifies the Region to connect to.</span></span>
<span data-ttu-id="a0156-124">Canary 지역이 아닌 한 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0156-124">Not used unless it is Canary region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0156-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0156-125">CommonParameters</span></span>
<span data-ttu-id="a0156-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a0156-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0156-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a0156-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0156-128">입력</span><span class="sxs-lookup"><span data-stu-id="a0156-128">INPUTS</span></span>

## <span data-ttu-id="a0156-129">출력</span><span class="sxs-lookup"><span data-stu-id="a0156-129">OUTPUTS</span></span>

### <span data-ttu-id="a0156-130">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="a0156-130">PSCustomObject.</span></span> <span data-ttu-id="a0156-131">PSCustomObject에서 다음 속성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a0156-131">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="a0156-132">테스트: 수행된 테스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a0156-132">Test: Name of the test performed.</span></span>
### <span data-ttu-id="a0156-133">EndpointTested: 테스트에 사용되는 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="a0156-133">EndpointTested: Endpoint used in the test.</span></span>
### <span data-ttu-id="a0156-134">IsRequired: True 또는 False</span><span class="sxs-lookup"><span data-stu-id="a0156-134">IsRequired: True or False</span></span>
### <span data-ttu-id="a0156-135">결과: 성공 또는 실패</span><span class="sxs-lookup"><span data-stu-id="a0156-135">Result: Succeeded or Failed</span></span>
### <span data-ttu-id="a0156-136">FailedNodes: 테스트가 실패한 노드 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a0156-136">FailedNodes: List of nodes on which the test failed.</span></span>
## <span data-ttu-id="a0156-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a0156-137">NOTES</span></span>

## <span data-ttu-id="a0156-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0156-138">RELATED LINKS</span></span>
