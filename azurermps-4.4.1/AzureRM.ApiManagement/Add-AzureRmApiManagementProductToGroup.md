---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
ms.openlocfilehash: b4e1a029eca4e7eda48f44d85292639767eaf845
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533219"
---
# <span data-ttu-id="fadd5-101">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="fadd5-101">Add-AzureRmApiManagementProductToGroup</span></span>

## <span data-ttu-id="fadd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fadd5-102">SYNOPSIS</span></span>
<span data-ttu-id="fadd5-103">그룹에 제품을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fadd5-103">Adds a product to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fadd5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fadd5-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fadd5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fadd5-105">DESCRIPTION</span></span>
<span data-ttu-id="fadd5-106">**Add-AzureRmApiManagementProductToGroup** cmdlet은 기존 그룹에 제품을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fadd5-106">The **Add-AzureRmApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="fadd5-107">즉,이 cmdlet은 그룹을 제품에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="fadd5-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="fadd5-108">예제의</span><span class="sxs-lookup"><span data-stu-id="fadd5-108">EXAMPLES</span></span>

### <span data-ttu-id="fadd5-109">예제 1: 그룹에 제품 추가</span><span class="sxs-lookup"><span data-stu-id="fadd5-109">Example 1: Add a product to a group</span></span>
```
PS C:\>Add-AzureRmApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="fadd5-110">이 명령은 기존 그룹에 제품을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fadd5-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="fadd5-111">변수</span><span class="sxs-lookup"><span data-stu-id="fadd5-111">PARAMETERS</span></span>

### <span data-ttu-id="fadd5-112">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="fadd5-112">-Context</span></span>
<span data-ttu-id="fadd5-113">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fadd5-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="fadd5-114">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="fadd5-114">This parameter is required.</span></span>

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

### <span data-ttu-id="fadd5-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="fadd5-115">-GroupId</span></span>
<span data-ttu-id="fadd5-116">그룹 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fadd5-116">Specifies the group ID.</span></span>
<span data-ttu-id="fadd5-117">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="fadd5-117">This parameter is required.</span></span>

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

### <span data-ttu-id="fadd5-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fadd5-118">-PassThru</span></span>
<span data-ttu-id="fadd5-119">passthru</span><span class="sxs-lookup"><span data-stu-id="fadd5-119">passthru</span></span>

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

### <span data-ttu-id="fadd5-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="fadd5-120">-ProductId</span></span>
<span data-ttu-id="fadd5-121">제품 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fadd5-121">Specifies the product ID.</span></span>
<span data-ttu-id="fadd5-122">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="fadd5-122">This parameter is required.</span></span>

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

### <span data-ttu-id="fadd5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fadd5-123">-DefaultProfile</span></span>
<span data-ttu-id="fadd5-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fadd5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fadd5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fadd5-125">CommonParameters</span></span>
<span data-ttu-id="fadd5-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fadd5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fadd5-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fadd5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fadd5-128">입력</span><span class="sxs-lookup"><span data-stu-id="fadd5-128">INPUTS</span></span>

## <span data-ttu-id="fadd5-129">출력</span><span class="sxs-lookup"><span data-stu-id="fadd5-129">OUTPUTS</span></span>

### <span data-ttu-id="fadd5-130">나타내는</span><span class="sxs-lookup"><span data-stu-id="fadd5-130">Boolean</span></span>

## <span data-ttu-id="fadd5-131">상속자</span><span class="sxs-lookup"><span data-stu-id="fadd5-131">NOTES</span></span>

## <span data-ttu-id="fadd5-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fadd5-132">RELATED LINKS</span></span>

[<span data-ttu-id="fadd5-133">제거-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="fadd5-133">Remove-AzureRmApiManagementProductFromGroup</span></span>](./Remove-AzureRmApiManagementProductFromGroup.md)


