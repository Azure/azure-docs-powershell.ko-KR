---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermprovideroperation
schema: 2.0.0
ms.openlocfilehash: 1274b04ed85917a9c1e185bfbef6307eaedecc05
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881730"
---
# <span data-ttu-id="32530-101">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="32530-101">Get-AzureRmProviderOperation</span></span>

## <span data-ttu-id="32530-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32530-102">SYNOPSIS</span></span>
<span data-ttu-id="32530-103">Azure RBAC를 사용 하 여 보안 할 수 있는 Azure resource provider에 대 한 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="32530-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32530-104">구문과</span><span class="sxs-lookup"><span data-stu-id="32530-104">SYNTAX</span></span>

```
Get-AzureRmProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="32530-105">설명은</span><span class="sxs-lookup"><span data-stu-id="32530-105">DESCRIPTION</span></span>
<span data-ttu-id="32530-106">Get-AzureRmProviderOperation Azure 리소스 공급자가 제공 하는 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="32530-106">The Get-AzureRmProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="32530-107">Azure RBAC에서 사용자 지정 역할을 만들기 위해 작업을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32530-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="32530-108">\*이 명령은 표시할 작업 세부 정보를 결정 하는 작업 검색 문자열 (가능한 와일드 카드 () 문자)을 입력으로 사용 합니다. Get-AzureRmProviderOperation *를 사용 하 여 모든 Azure 리소스 공급자에 대 한 모든 작업을 가져옵니다. Microsoft. Compute/Get-AzureRmProviderOperation를 사용 하 여* microsoft의 모든 작업 (compute resource provider)을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="32530-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzureRmProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzureRmProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="32530-109">예제의</span><span class="sxs-lookup"><span data-stu-id="32530-109">EXAMPLES</span></span>

### <span data-ttu-id="32530-110">모든 공급자에 대 한 모든 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="32530-110">Get all actions for all providers</span></span>
```
PS C:\> Get-AzureRmProviderOperation *
```

### <span data-ttu-id="32530-111">특정 리소스 공급자에 대 한 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="32530-111">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="32530-112">가상 컴퓨터에서 수행할 수 있는 모든 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="32530-112">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## <span data-ttu-id="32530-113">변수</span><span class="sxs-lookup"><span data-stu-id="32530-113">PARAMETERS</span></span>

### <span data-ttu-id="32530-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32530-114">-DefaultProfile</span></span>
<span data-ttu-id="32530-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="32530-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32530-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="32530-116">-OperationSearchString</span></span>
<span data-ttu-id="32530-117">작업 검색 문자열 (와일드 카드 (\*) 문자 사용 가능)</span><span class="sxs-lookup"><span data-stu-id="32530-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="32530-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32530-118">CommonParameters</span></span>
<span data-ttu-id="32530-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="32530-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32530-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32530-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32530-121">입력</span><span class="sxs-lookup"><span data-stu-id="32530-121">INPUTS</span></span>

### <span data-ttu-id="32530-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="32530-122">System.String</span></span>
<span data-ttu-id="32530-123">매개 변수: OperationSearchString (ByValue)</span><span class="sxs-lookup"><span data-stu-id="32530-123">Parameters: OperationSearchString (ByValue)</span></span>

## <span data-ttu-id="32530-124">출력</span><span class="sxs-lookup"><span data-stu-id="32530-124">OUTPUTS</span></span>

### <span data-ttu-id="32530-125">Microsoft. PSResourceProviderOperation (.Resources)</span><span class="sxs-lookup"><span data-stu-id="32530-125">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="32530-126">상속자</span><span class="sxs-lookup"><span data-stu-id="32530-126">NOTES</span></span>
<span data-ttu-id="32530-127">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="32530-127">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="32530-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32530-128">RELATED LINKS</span></span>
