---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: bffe2874effb99b3fbcca77888a3108bc3798311
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332102"
---
# <span data-ttu-id="9c3ba-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="9c3ba-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="9c3ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c3ba-102">SYNOPSIS</span></span>
<span data-ttu-id="9c3ba-103">Azure RBAC를 사용하여 보안이 가능한 Azure 리소스 공급자에 대한 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9c3ba-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="9c3ba-104">구문</span><span class="sxs-lookup"><span data-stu-id="9c3ba-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c3ba-105">설명</span><span class="sxs-lookup"><span data-stu-id="9c3ba-105">DESCRIPTION</span></span>
<span data-ttu-id="9c3ba-106">이 Get-AzProviderOperation Azure 리소스 공급자가 노출하는 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9c3ba-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="9c3ba-107">Azure RBAC에서 사용자 지정 역할을 만들기 위해 작업을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9c3ba-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="9c3ba-108">이 명령은 표시할 작업 세부 정보를 결정하는 작업 검색 문자열(가능한 와일드카드( ) 문자가 있는)을 입력으로 \*사용하게 됩니다. Get-AzProviderOperation *를 사용하여 모든 Azure 리소스 공급자에 대한 모든 작업을 얻습니다. Microsoft.compute/Get-AzProviderOperation 사용하여* Microsoft.Compute 리소스 공급자의 모든 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9c3ba-108">The command takes as input an operation search string (with possible wildcard(*) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="9c3ba-109">예제</span><span class="sxs-lookup"><span data-stu-id="9c3ba-109">EXAMPLES</span></span>

### <span data-ttu-id="9c3ba-110">예제 1: 모든 공급자에 대한 모든 작업 수행</span><span class="sxs-lookup"><span data-stu-id="9c3ba-110">Example 1: Get all actions for all providers</span></span>
```powershell
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="9c3ba-111">예제 2: 특정 리소스 공급자에 대한 작업 수행</span><span class="sxs-lookup"><span data-stu-id="9c3ba-111">Example 2: Get actions for a particular resource provider</span></span>
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="9c3ba-112">예제 3: 가상 머신에서 수행할 수 있는 모든 작업 수행</span><span class="sxs-lookup"><span data-stu-id="9c3ba-112">Example 3: Get all actions that can be performed on virtual machines</span></span>
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="9c3ba-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c3ba-113">PARAMETERS</span></span>

### <span data-ttu-id="9c3ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c3ba-114">-DefaultProfile</span></span>
<span data-ttu-id="9c3ba-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9c3ba-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c3ba-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="9c3ba-116">-OperationSearchString</span></span>
<span data-ttu-id="9c3ba-117">작업 검색 문자열(가능한 와일드카드(\*) 문자 사용)</span><span class="sxs-lookup"><span data-stu-id="9c3ba-117">The operation search string (with possible wildcard (\*) characters)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c3ba-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c3ba-118">CommonParameters</span></span>
<span data-ttu-id="9c3ba-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9c3ba-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c3ba-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9c3ba-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c3ba-121">입력</span><span class="sxs-lookup"><span data-stu-id="9c3ba-121">INPUTS</span></span>

### <span data-ttu-id="9c3ba-122">System.String</span><span class="sxs-lookup"><span data-stu-id="9c3ba-122">System.String</span></span>

## <span data-ttu-id="9c3ba-123">출력</span><span class="sxs-lookup"><span data-stu-id="9c3ba-123">OUTPUTS</span></span>

### <span data-ttu-id="9c3ba-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="9c3ba-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="9c3ba-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9c3ba-125">NOTES</span></span>
<span data-ttu-id="9c3ba-126">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포</span><span class="sxs-lookup"><span data-stu-id="9c3ba-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="9c3ba-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9c3ba-127">RELATED LINKS</span></span>
