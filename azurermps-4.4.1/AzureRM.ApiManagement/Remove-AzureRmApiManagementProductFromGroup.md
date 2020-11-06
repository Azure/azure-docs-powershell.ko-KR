---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
ms.openlocfilehash: a6ef7e141863b6dfd98185df0f8e3cfbd85ae40b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525768"
---
# <span data-ttu-id="a5dc8-101">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="a5dc8-101">Remove-AzureRmApiManagementProductFromGroup</span></span>

## <span data-ttu-id="a5dc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="a5dc8-103">그룹에서 제품을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5dc8-103">Removes a product from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5dc8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5dc8-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String>
 -ProductId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5dc8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a5dc8-105">DESCRIPTION</span></span>
<span data-ttu-id="a5dc8-106">**AzureRmApiManagementProductFromGroup** cmdlet은 기존 그룹의 제품을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5dc8-106">The **Remove-AzureRmApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="a5dc8-107">즉,이 cmdlet은 제품에서 그룹 과제를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5dc8-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="a5dc8-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a5dc8-108">EXAMPLES</span></span>

### <span data-ttu-id="a5dc8-109">예제 1: 그룹에서 제품 제거</span><span class="sxs-lookup"><span data-stu-id="a5dc8-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>Remove-AzureRmApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="a5dc8-110">이 명령은 기존 그룹에서 제품을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5dc8-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="a5dc8-111">변수</span><span class="sxs-lookup"><span data-stu-id="a5dc8-111">PARAMETERS</span></span>

### <span data-ttu-id="a5dc8-112">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="a5dc8-112">-Context</span></span>
<span data-ttu-id="a5dc8-113">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5dc8-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="a5dc8-114">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a5dc8-114">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5dc8-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="a5dc8-115">-GroupId</span></span>
<span data-ttu-id="a5dc8-116">그룹 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5dc8-116">Specifies the group ID.</span></span>
<span data-ttu-id="a5dc8-117">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a5dc8-117">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5dc8-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5dc8-118">-PassThru</span></span>
<span data-ttu-id="a5dc8-119">이 cmdlet이 $True 값을 반환 하거나, 성공할 경우, $False 또는, 그렇지 않은 경우이를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a5dc8-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5dc8-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="a5dc8-120">-ProductId</span></span>
<span data-ttu-id="a5dc8-121">제품 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5dc8-121">Specifies the product ID.</span></span>
<span data-ttu-id="a5dc8-122">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a5dc8-122">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5dc8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5dc8-123">-DefaultProfile</span></span>
<span data-ttu-id="a5dc8-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5dc8-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5dc8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5dc8-125">CommonParameters</span></span>
<span data-ttu-id="a5dc8-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5dc8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5dc8-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5dc8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5dc8-128">입력</span><span class="sxs-lookup"><span data-stu-id="a5dc8-128">INPUTS</span></span>

## <span data-ttu-id="a5dc8-129">출력</span><span class="sxs-lookup"><span data-stu-id="a5dc8-129">OUTPUTS</span></span>

### <span data-ttu-id="a5dc8-130">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a5dc8-130">System.Boolean</span></span>

## <span data-ttu-id="a5dc8-131">상속자</span><span class="sxs-lookup"><span data-stu-id="a5dc8-131">NOTES</span></span>

## <span data-ttu-id="a5dc8-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5dc8-132">RELATED LINKS</span></span>

[<span data-ttu-id="a5dc8-133">추가-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="a5dc8-133">Add-AzureRmApiManagementProductToGroup</span></span>](./Add-AzureRmApiManagementProductToGroup.md)


