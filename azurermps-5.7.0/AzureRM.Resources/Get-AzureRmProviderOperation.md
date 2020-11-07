---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
ms.openlocfilehash: 51229c966c0e4c8b0ec74c3c940037aca5081b15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704008"
---
# <span data-ttu-id="5ab1a-101">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="5ab1a-101">Get-AzureRmProviderOperation</span></span>

## <span data-ttu-id="5ab1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ab1a-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab1a-103">Azure RBAC를 사용 하 여 보안 할 수 있는 Azure resource provider에 대 한 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ab1a-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ab1a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5ab1a-104">SYNTAX</span></span>

```
Get-AzureRmProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ab1a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5ab1a-105">DESCRIPTION</span></span>
<span data-ttu-id="5ab1a-106">Get-AzureRmProviderOperation Azure 리소스 공급자가 제공 하는 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ab1a-106">The Get-AzureRmProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="5ab1a-107">Azure RBAC에서 사용자 지정 역할을 만들기 위해 작업을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5ab1a-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="5ab1a-108">명령이 표시할 작업 세부 정보를 결정 하는 작업 검색 문자열 (가능한 와일드 카드 (\*) 문자)을 입력으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ab1a-108">The command takes as input an operation search string (with possible wildcard(\*) character(s)) which determines the operations details to display.</span></span>

<span data-ttu-id="5ab1a-109">Get-AzureRmProviderOperation \*를 사용 하 여 모든 Azure 리소스 공급자에 대 한 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ab1a-109">Use Get-AzureRmProviderOperation \* to get all operations for all Azure resource providers.</span></span>

<span data-ttu-id="5ab1a-110">Microsoft. Compute/\* Get-AzureRmProviderOperation를 사용 하 여 리소스 공급자의 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ab1a-110">Use Get-AzureRmProviderOperation Microsoft.Compute/\* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="5ab1a-111">예제의</span><span class="sxs-lookup"><span data-stu-id="5ab1a-111">EXAMPLES</span></span>

### <span data-ttu-id="5ab1a-112">모든 공급자에 대 한 모든 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="5ab1a-112">Get all actions for all providers</span></span>
```
PS C:\> Get-AzureRmProviderOperation *
```

### <span data-ttu-id="5ab1a-113">특정 리소스 공급자에 대 한 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="5ab1a-113">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="5ab1a-114">가상 컴퓨터에서 수행할 수 있는 모든 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="5ab1a-114">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## <span data-ttu-id="5ab1a-115">변수</span><span class="sxs-lookup"><span data-stu-id="5ab1a-115">PARAMETERS</span></span>

### <span data-ttu-id="5ab1a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ab1a-116">-DefaultProfile</span></span>
<span data-ttu-id="5ab1a-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5ab1a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab1a-118">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="5ab1a-118">-OperationSearchString</span></span>
<span data-ttu-id="5ab1a-119">작업 검색 문자열 (와일드 카드 (\*) 문자 사용 가능)</span><span class="sxs-lookup"><span data-stu-id="5ab1a-119">The operation search string (with possible wildcard (\*) characters)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ab1a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab1a-120">CommonParameters</span></span>
<span data-ttu-id="5ab1a-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ab1a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab1a-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ab1a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab1a-123">입력</span><span class="sxs-lookup"><span data-stu-id="5ab1a-123">INPUTS</span></span>

### <span data-ttu-id="5ab1a-124">이름</span><span class="sxs-lookup"><span data-stu-id="5ab1a-124">String</span></span>
<span data-ttu-id="5ab1a-125">' OperationSearchString ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ab1a-125">Parameter 'OperationSearchString' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5ab1a-126">출력</span><span class="sxs-lookup"><span data-stu-id="5ab1a-126">OUTPUTS</span></span>

### <span data-ttu-id="5ab1a-127">Microsoft. PSResourceProviderOperation (.Resources)</span><span class="sxs-lookup"><span data-stu-id="5ab1a-127">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="5ab1a-128">상속자</span><span class="sxs-lookup"><span data-stu-id="5ab1a-128">NOTES</span></span>
<span data-ttu-id="5ab1a-129">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="5ab1a-129">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="5ab1a-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ab1a-130">RELATED LINKS</span></span>
