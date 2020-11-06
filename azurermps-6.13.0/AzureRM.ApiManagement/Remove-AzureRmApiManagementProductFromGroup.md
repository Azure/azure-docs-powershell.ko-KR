---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
ms.openlocfilehash: 0d56528f2cbe827f4dfc5ba20e2a9f8c840256ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533475"
---
# <span data-ttu-id="46259-101">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="46259-101">Remove-AzureRmApiManagementProductFromGroup</span></span>

## <span data-ttu-id="46259-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46259-102">SYNOPSIS</span></span>
<span data-ttu-id="46259-103">그룹에서 제품을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="46259-103">Removes a product from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46259-104">구문과</span><span class="sxs-lookup"><span data-stu-id="46259-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String>
 -ProductId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46259-105">설명은</span><span class="sxs-lookup"><span data-stu-id="46259-105">DESCRIPTION</span></span>
<span data-ttu-id="46259-106">**AzureRmApiManagementProductFromGroup** cmdlet은 기존 그룹의 제품을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="46259-106">The **Remove-AzureRmApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="46259-107">즉,이 cmdlet은 제품에서 그룹 과제를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="46259-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="46259-108">예제의</span><span class="sxs-lookup"><span data-stu-id="46259-108">EXAMPLES</span></span>

### <span data-ttu-id="46259-109">예제 1: 그룹에서 제품 제거</span><span class="sxs-lookup"><span data-stu-id="46259-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="46259-110">이 명령은 기존 그룹에서 제품을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="46259-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="46259-111">변수</span><span class="sxs-lookup"><span data-stu-id="46259-111">PARAMETERS</span></span>

### <span data-ttu-id="46259-112">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="46259-112">-Context</span></span>
<span data-ttu-id="46259-113">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46259-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="46259-114">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="46259-114">This parameter is required.</span></span>

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

### <span data-ttu-id="46259-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46259-115">-DefaultProfile</span></span>
<span data-ttu-id="46259-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="46259-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46259-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="46259-117">-GroupId</span></span>
<span data-ttu-id="46259-118">그룹 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46259-118">Specifies the group ID.</span></span>
<span data-ttu-id="46259-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="46259-119">This parameter is required.</span></span>

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

### <span data-ttu-id="46259-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46259-120">-PassThru</span></span>
<span data-ttu-id="46259-121">이 cmdlet이 $True 값을 반환 하거나, 성공할 경우, $False 또는, 그렇지 않은 경우이를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="46259-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="46259-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="46259-122">-ProductId</span></span>
<span data-ttu-id="46259-123">제품 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46259-123">Specifies the product ID.</span></span>
<span data-ttu-id="46259-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="46259-124">This parameter is required.</span></span>

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

### <span data-ttu-id="46259-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46259-125">CommonParameters</span></span>
<span data-ttu-id="46259-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="46259-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46259-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46259-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46259-128">입력</span><span class="sxs-lookup"><span data-stu-id="46259-128">INPUTS</span></span>

### <span data-ttu-id="46259-129">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="46259-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="46259-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="46259-130">System.String</span></span>

### <span data-ttu-id="46259-131">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="46259-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="46259-132">출력</span><span class="sxs-lookup"><span data-stu-id="46259-132">OUTPUTS</span></span>

### <span data-ttu-id="46259-133">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="46259-133">System.Boolean</span></span>

## <span data-ttu-id="46259-134">상속자</span><span class="sxs-lookup"><span data-stu-id="46259-134">NOTES</span></span>

## <span data-ttu-id="46259-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46259-135">RELATED LINKS</span></span>

[<span data-ttu-id="46259-136">추가-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="46259-136">Add-AzureRmApiManagementProductToGroup</span></span>](./Add-AzureRmApiManagementProductToGroup.md)


