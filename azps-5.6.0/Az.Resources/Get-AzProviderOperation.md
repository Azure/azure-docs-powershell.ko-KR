---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 61e38afcccccd6a96e92983d24442740351320ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016043"
---
# <span data-ttu-id="982aa-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="982aa-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="982aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="982aa-102">SYNOPSIS</span></span>
<span data-ttu-id="982aa-103">Azure RBAC를 사용하여 보안이 가능한 Azure 리소스 공급자에 대한 작업을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="982aa-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="982aa-104">구문</span><span class="sxs-lookup"><span data-stu-id="982aa-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="982aa-105">설명</span><span class="sxs-lookup"><span data-stu-id="982aa-105">DESCRIPTION</span></span>
<span data-ttu-id="982aa-106">이 Get-AzProviderOperation Azure 리소스 공급자에 의해 노출되는 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="982aa-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="982aa-107">작업을 구성하여 Azure RBAC에서 사용자 지정 역할을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="982aa-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="982aa-108">명령은 표시할 작업 세부 정보를 결정하는 작업 검색 문자열(가능한 와일드카드() 문자)를 입력으로 *합니다. Get-AzProviderOperation \* 를 사용하여 모든 Azure 리소스 공급자에 대한 모든 작업을 얻습니다. Microsoft.Compute/Get-AzProviderOperation Microsoft.Compute* 리소스 공급자의 모든 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="982aa-108">The command takes as input an operation search string (with possible wildcard(*) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="982aa-109">예제</span><span class="sxs-lookup"><span data-stu-id="982aa-109">EXAMPLES</span></span>

### <span data-ttu-id="982aa-110">예제 1: 모든 공급자에 대한 모든 작업 수행</span><span class="sxs-lookup"><span data-stu-id="982aa-110">Example 1: Get all actions for all providers</span></span>
```powershell
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="982aa-111">예제 2: 특정 리소스 공급자에 대한 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="982aa-111">Example 2: Get actions for a particular resource provider</span></span>
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="982aa-112">예제 3: 가상 머신에서 수행할 수 있는 모든 작업</span><span class="sxs-lookup"><span data-stu-id="982aa-112">Example 3: Get all actions that can be performed on virtual machines</span></span>
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="982aa-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="982aa-113">PARAMETERS</span></span>

### <span data-ttu-id="982aa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="982aa-114">-DefaultProfile</span></span>
<span data-ttu-id="982aa-115">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="982aa-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="982aa-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="982aa-116">-OperationSearchString</span></span>
<span data-ttu-id="982aa-117">작업 검색 문자열(와일드카드(\*) 문자가 있는 경우)</span><span class="sxs-lookup"><span data-stu-id="982aa-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="982aa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="982aa-118">CommonParameters</span></span>
<span data-ttu-id="982aa-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="982aa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="982aa-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="982aa-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="982aa-121">입력</span><span class="sxs-lookup"><span data-stu-id="982aa-121">INPUTS</span></span>

### <span data-ttu-id="982aa-122">System.String</span><span class="sxs-lookup"><span data-stu-id="982aa-122">System.String</span></span>

## <span data-ttu-id="982aa-123">출력</span><span class="sxs-lookup"><span data-stu-id="982aa-123">OUTPUTS</span></span>

### <span data-ttu-id="982aa-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="982aa-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="982aa-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="982aa-125">NOTES</span></span>
<span data-ttu-id="982aa-126">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포</span><span class="sxs-lookup"><span data-stu-id="982aa-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="982aa-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="982aa-127">RELATED LINKS</span></span>
