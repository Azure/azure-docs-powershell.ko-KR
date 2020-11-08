---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
ms.openlocfilehash: c06442ef9ab4b5f80943da33ed87fc24c276107d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204138"
---
# <span data-ttu-id="83dc7-101">New-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="83dc7-101">New-AzApiManagementGateway</span></span>

## <span data-ttu-id="83dc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="83dc7-103">새 게이트웨이 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="83dc7-103">Creates new Gateway entity.</span></span>

## <span data-ttu-id="83dc7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="83dc7-104">SYNTAX</span></span>

```
New-AzApiManagementGateway -Context <PsApiManagementContext> [-GatewayId <String>] [-Description <String>]
 -LocationData <PsApiManagementResourceLocation> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83dc7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="83dc7-105">DESCRIPTION</span></span>
<span data-ttu-id="83dc7-106">새 게이트웨이 엔터티를 만드는 **AzApiManagementGateway** cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83dc7-106">The **New-AzApiManagementGateway** cmdlet creates new Gateway entity.</span></span>

## <span data-ttu-id="83dc7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="83dc7-107">EXAMPLES</span></span>

### <span data-ttu-id="83dc7-108">예제 1: 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="83dc7-108">Example 1: Create a gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
PS C:\>New-AzApiManagementGateway -Context $apimContext -GatewayId "123" -Description "desc" -LocationData $location
```

<span data-ttu-id="83dc7-109">이 명령은 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="83dc7-109">This command creates a gateway.</span></span>

## <span data-ttu-id="83dc7-110">변수</span><span class="sxs-lookup"><span data-stu-id="83dc7-110">PARAMETERS</span></span>

### <span data-ttu-id="83dc7-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="83dc7-111">-Context</span></span>
<span data-ttu-id="83dc7-112">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="83dc7-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="83dc7-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="83dc7-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83dc7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83dc7-114">-DefaultProfile</span></span>
<span data-ttu-id="83dc7-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83dc7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83dc7-116">-설명</span><span class="sxs-lookup"><span data-stu-id="83dc7-116">-Description</span></span>
<span data-ttu-id="83dc7-117">게이트웨이 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="83dc7-117">Gateway description.</span></span>
<span data-ttu-id="83dc7-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="83dc7-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83dc7-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="83dc7-119">-GatewayId</span></span>
<span data-ttu-id="83dc7-120">새 게이트웨이의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="83dc7-120">Identifier of new gateway.</span></span>
<span data-ttu-id="83dc7-121">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="83dc7-121">This parameter is optional.</span></span>
<span data-ttu-id="83dc7-122">지정 하지 않으면가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="83dc7-122">If not specified will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83dc7-123">-LocationData</span><span class="sxs-lookup"><span data-stu-id="83dc7-123">-LocationData</span></span>
<span data-ttu-id="83dc7-124">게이트웨이 위치.</span><span class="sxs-lookup"><span data-stu-id="83dc7-124">Gateway location.</span></span>
<span data-ttu-id="83dc7-125">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="83dc7-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83dc7-126">-확인</span><span class="sxs-lookup"><span data-stu-id="83dc7-126">-Confirm</span></span>
<span data-ttu-id="83dc7-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="83dc7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83dc7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83dc7-128">-WhatIf</span></span>
<span data-ttu-id="83dc7-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="83dc7-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83dc7-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83dc7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83dc7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83dc7-131">CommonParameters</span></span>
<span data-ttu-id="83dc7-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="83dc7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83dc7-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="83dc7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83dc7-134">입력</span><span class="sxs-lookup"><span data-stu-id="83dc7-134">INPUTS</span></span>

### <span data-ttu-id="83dc7-135">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="83dc7-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="83dc7-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="83dc7-136">System.String</span></span>

### <span data-ttu-id="83dc7-137">ApiManagement. ServiceManagement. \ PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="83dc7-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="83dc7-138">출력</span><span class="sxs-lookup"><span data-stu-id="83dc7-138">OUTPUTS</span></span>

### <span data-ttu-id="83dc7-139">ApiManagement. ServiceManagement. \ PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="83dc7-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="83dc7-140">상속자</span><span class="sxs-lookup"><span data-stu-id="83dc7-140">NOTES</span></span>

## <span data-ttu-id="83dc7-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83dc7-141">RELATED LINKS</span></span>
