---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
ms.openlocfilehash: c06442ef9ab4b5f80943da33ed87fc24c276107d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332342"
---
# <span data-ttu-id="5d599-101">New-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="5d599-101">New-AzApiManagementGateway</span></span>

## <span data-ttu-id="5d599-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d599-102">SYNOPSIS</span></span>
<span data-ttu-id="5d599-103">새 게이트웨이 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d599-103">Creates new Gateway entity.</span></span>

## <span data-ttu-id="5d599-104">구문</span><span class="sxs-lookup"><span data-stu-id="5d599-104">SYNTAX</span></span>

```
New-AzApiManagementGateway -Context <PsApiManagementContext> [-GatewayId <String>] [-Description <String>]
 -LocationData <PsApiManagementResourceLocation> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d599-105">설명</span><span class="sxs-lookup"><span data-stu-id="5d599-105">DESCRIPTION</span></span>
<span data-ttu-id="5d599-106">**New-AzApiManagementGateway** cmdlet은 새 게이트웨이 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d599-106">The **New-AzApiManagementGateway** cmdlet creates new Gateway entity.</span></span>

## <span data-ttu-id="5d599-107">예제</span><span class="sxs-lookup"><span data-stu-id="5d599-107">EXAMPLES</span></span>

### <span data-ttu-id="5d599-108">예제 1: 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="5d599-108">Example 1: Create a gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
PS C:\>New-AzApiManagementGateway -Context $apimContext -GatewayId "123" -Description "desc" -LocationData $location
```

<span data-ttu-id="5d599-109">이 명령은 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d599-109">This command creates a gateway.</span></span>

## <span data-ttu-id="5d599-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d599-110">PARAMETERS</span></span>

### <span data-ttu-id="5d599-111">-Context</span><span class="sxs-lookup"><span data-stu-id="5d599-111">-Context</span></span>
<span data-ttu-id="5d599-112">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="5d599-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5d599-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5d599-113">This parameter is required.</span></span>

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

### <span data-ttu-id="5d599-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d599-114">-DefaultProfile</span></span>
<span data-ttu-id="5d599-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d599-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d599-116">-Description</span><span class="sxs-lookup"><span data-stu-id="5d599-116">-Description</span></span>
<span data-ttu-id="5d599-117">게이트웨이 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="5d599-117">Gateway description.</span></span>
<span data-ttu-id="5d599-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5d599-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="5d599-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="5d599-119">-GatewayId</span></span>
<span data-ttu-id="5d599-120">새 게이트웨이의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5d599-120">Identifier of new gateway.</span></span>
<span data-ttu-id="5d599-121">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5d599-121">This parameter is optional.</span></span>
<span data-ttu-id="5d599-122">지정하지 않으면 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d599-122">If not specified will be generated.</span></span>

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

### <span data-ttu-id="5d599-123">-LocationData</span><span class="sxs-lookup"><span data-stu-id="5d599-123">-LocationData</span></span>
<span data-ttu-id="5d599-124">게이트웨이 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="5d599-124">Gateway location.</span></span>
<span data-ttu-id="5d599-125">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5d599-125">This parameter is required.</span></span>

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

### <span data-ttu-id="5d599-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d599-126">-Confirm</span></span>
<span data-ttu-id="5d599-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d599-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d599-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d599-128">-WhatIf</span></span>
<span data-ttu-id="5d599-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5d599-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d599-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d599-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d599-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d599-131">CommonParameters</span></span>
<span data-ttu-id="5d599-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d599-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d599-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5d599-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d599-134">입력</span><span class="sxs-lookup"><span data-stu-id="5d599-134">INPUTS</span></span>

### <span data-ttu-id="5d599-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5d599-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5d599-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5d599-136">System.String</span></span>

### <span data-ttu-id="5d599-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="5d599-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="5d599-138">출력</span><span class="sxs-lookup"><span data-stu-id="5d599-138">OUTPUTS</span></span>

### <span data-ttu-id="5d599-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="5d599-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="5d599-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5d599-140">NOTES</span></span>

## <span data-ttu-id="5d599-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d599-141">RELATED LINKS</span></span>
