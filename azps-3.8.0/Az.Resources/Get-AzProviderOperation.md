---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 1ee29a4183dd78e9ced6d48e5f52c724e1b9a985
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042617"
---
# <span data-ttu-id="d9f9c-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="d9f9c-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="d9f9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9f9c-102">SYNOPSIS</span></span>
<span data-ttu-id="d9f9c-103">Azure RBAC를 사용 하 여 보안 할 수 있는 Azure resource provider에 대 한 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9f9c-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="d9f9c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d9f9c-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9f9c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d9f9c-105">DESCRIPTION</span></span>
<span data-ttu-id="d9f9c-106">Get-AzProviderOperation Azure 리소스 공급자가 제공 하는 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9f9c-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="d9f9c-107">Azure RBAC에서 사용자 지정 역할을 만들기 위해 작업을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9f9c-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="d9f9c-108">\*이 명령은 표시할 작업 세부 정보를 결정 하는 작업 검색 문자열 (가능한 와일드 카드 () 문자)을 입력으로 사용 합니다. Get-AzProviderOperation *를 사용 하 여 모든 Azure 리소스 공급자에 대 한 모든 작업을 가져옵니다. Microsoft. Compute/Get-AzProviderOperation를 사용 하 여* microsoft의 모든 작업 (compute resource provider)을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9f9c-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="d9f9c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d9f9c-109">EXAMPLES</span></span>

### <span data-ttu-id="d9f9c-110">모든 공급자에 대 한 모든 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="d9f9c-110">Get all actions for all providers</span></span>
```
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="d9f9c-111">특정 리소스 공급자에 대 한 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="d9f9c-111">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="d9f9c-112">가상 컴퓨터에서 수행할 수 있는 모든 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="d9f9c-112">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="d9f9c-113">변수</span><span class="sxs-lookup"><span data-stu-id="d9f9c-113">PARAMETERS</span></span>

### <span data-ttu-id="d9f9c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9f9c-114">-DefaultProfile</span></span>
<span data-ttu-id="d9f9c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d9f9c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9f9c-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="d9f9c-116">-OperationSearchString</span></span>
<span data-ttu-id="d9f9c-117">작업 검색 문자열 (와일드 카드 (\*) 문자 사용 가능)</span><span class="sxs-lookup"><span data-stu-id="d9f9c-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="d9f9c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9f9c-118">CommonParameters</span></span>
<span data-ttu-id="d9f9c-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9f9c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9f9c-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d9f9c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9f9c-121">입력</span><span class="sxs-lookup"><span data-stu-id="d9f9c-121">INPUTS</span></span>

### <span data-ttu-id="d9f9c-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d9f9c-122">System.String</span></span>

## <span data-ttu-id="d9f9c-123">출력</span><span class="sxs-lookup"><span data-stu-id="d9f9c-123">OUTPUTS</span></span>

### <span data-ttu-id="d9f9c-124">Microsoft. PSResourceProviderOperation (.Resources)</span><span class="sxs-lookup"><span data-stu-id="d9f9c-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="d9f9c-125">상속자</span><span class="sxs-lookup"><span data-stu-id="d9f9c-125">NOTES</span></span>
<span data-ttu-id="d9f9c-126">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="d9f9c-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d9f9c-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9f9c-127">RELATED LINKS</span></span>
