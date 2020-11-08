---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/Update-AzApiManagementGateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
ms.openlocfilehash: d053bc60390c43c3409bb7adfad5a3ff3720f5b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047984"
---
# <span data-ttu-id="a44e4-101">Update-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="a44e4-101">Update-AzApiManagementGateway</span></span>

## <span data-ttu-id="a44e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a44e4-102">SYNOPSIS</span></span>
<span data-ttu-id="a44e4-103">API management 게이트웨이를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a44e4-103">Configures an API management Gateway.</span></span>

## <span data-ttu-id="a44e4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a44e4-104">SYNTAX</span></span>

### <span data-ttu-id="a44e4-105">ExpandedParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="a44e4-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a44e4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a44e4-106">ByInputObject</span></span>
```
Update-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a44e4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a44e4-107">ByResourceId</span></span>
```
Update-AzApiManagementGateway -ResourceId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a44e4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a44e4-108">DESCRIPTION</span></span>
<span data-ttu-id="a44e4-109">**업데이트 AzApiManagementGateway** CMDLET은 API management 게이트웨이를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a44e4-109">The **Update-AzApiManagementGateway** cmdlet configures an API management Gateway.</span></span>

## <span data-ttu-id="a44e4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a44e4-110">EXAMPLES</span></span>

### <span data-ttu-id="a44e4-111">예제 1: 관리 그룹 구성</span><span class="sxs-lookup"><span data-stu-id="a44e4-111">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementGateway -Context $apimContext -GatewayId "0001" -Description "Updated Gateway"
```

<span data-ttu-id="a44e4-112">이 명령은 게이트웨이를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a44e4-112">This command configures a gateway.</span></span>

## <span data-ttu-id="a44e4-113">변수</span><span class="sxs-lookup"><span data-stu-id="a44e4-113">PARAMETERS</span></span>

### <span data-ttu-id="a44e4-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="a44e4-114">-Context</span></span>
<span data-ttu-id="a44e4-115">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="a44e4-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a44e4-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a44e4-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a44e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a44e4-117">-DefaultProfile</span></span>
<span data-ttu-id="a44e4-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a44e4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a44e4-119">-설명</span><span class="sxs-lookup"><span data-stu-id="a44e4-119">-Description</span></span>
<span data-ttu-id="a44e4-120">게이트웨이 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="a44e4-120">Gateway description.</span></span>
<span data-ttu-id="a44e4-121">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a44e4-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="a44e4-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="a44e4-122">-GatewayId</span></span>
<span data-ttu-id="a44e4-123">기존 게이트웨이의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a44e4-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="a44e4-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a44e4-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a44e4-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a44e4-125">-InputObject</span></span>
<span data-ttu-id="a44e4-126">PsApiManagementGateway의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="a44e4-126">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="a44e4-127">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a44e4-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a44e4-128">-LocationData</span><span class="sxs-lookup"><span data-stu-id="a44e4-128">-LocationData</span></span>
<span data-ttu-id="a44e4-129">게이트웨이 위치.</span><span class="sxs-lookup"><span data-stu-id="a44e4-129">Gateway location.</span></span>
<span data-ttu-id="a44e4-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a44e4-130">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a44e4-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a44e4-131">-PassThru</span></span>
<span data-ttu-id="a44e4-132">지정 된 경우 ApiManagement의 인스턴스가 수정 된 게이트웨이를 나타내는 ServiceManagement 유형의 PsApiManagementGateway 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a44e4-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway type representing the modified gateway.</span></span>

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

### <span data-ttu-id="a44e4-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a44e4-133">-ResourceId</span></span>
<span data-ttu-id="a44e4-134">게이트웨이의 팔 인 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="a44e4-134">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="a44e4-135">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a44e4-135">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a44e4-136">-확인</span><span class="sxs-lookup"><span data-stu-id="a44e4-136">-Confirm</span></span>
<span data-ttu-id="a44e4-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a44e4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a44e4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a44e4-138">-WhatIf</span></span>
<span data-ttu-id="a44e4-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a44e4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a44e4-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a44e4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a44e4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a44e4-141">CommonParameters</span></span>
<span data-ttu-id="a44e4-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a44e4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a44e4-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a44e4-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a44e4-144">입력</span><span class="sxs-lookup"><span data-stu-id="a44e4-144">INPUTS</span></span>

### <span data-ttu-id="a44e4-145">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a44e4-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a44e4-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a44e4-146">System.String</span></span>

### <span data-ttu-id="a44e4-147">ApiManagement. ServiceManagement. \ PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="a44e4-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

### <span data-ttu-id="a44e4-148">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a44e4-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a44e4-149">출력</span><span class="sxs-lookup"><span data-stu-id="a44e4-149">OUTPUTS</span></span>

### <span data-ttu-id="a44e4-150">ApiManagement. ServiceManagement. \ PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="a44e4-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="a44e4-151">상속자</span><span class="sxs-lookup"><span data-stu-id="a44e4-151">NOTES</span></span>

## <span data-ttu-id="a44e4-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a44e4-152">RELATED LINKS</span></span>
