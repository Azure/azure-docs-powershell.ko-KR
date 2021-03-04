---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: d1ef516fc8b95814685350eb309e0a56d08d4b59
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959115"
---
# <span data-ttu-id="a591a-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a591a-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="a591a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a591a-102">SYNOPSIS</span></span>
<span data-ttu-id="a591a-103">API를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a591a-103">Removes an API.</span></span>

## <span data-ttu-id="a591a-104">구문</span><span class="sxs-lookup"><span data-stu-id="a591a-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a591a-105">설명</span><span class="sxs-lookup"><span data-stu-id="a591a-105">DESCRIPTION</span></span>
<span data-ttu-id="a591a-106">**Remove-AzApiManagementApi** cmdlet은 기존 API를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a591a-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="a591a-107">예제</span><span class="sxs-lookup"><span data-stu-id="a591a-107">EXAMPLES</span></span>

### <span data-ttu-id="a591a-108">예제 1: API 제거</span><span class="sxs-lookup"><span data-stu-id="a591a-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="a591a-109">이 명령은 지정된 ID를 사용하여 API를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a591a-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="a591a-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a591a-110">PARAMETERS</span></span>

### <span data-ttu-id="a591a-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a591a-111">-ApiId</span></span>
<span data-ttu-id="a591a-112">API 제거의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a591a-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="a591a-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a591a-113">-Context</span></span>
<span data-ttu-id="a591a-114">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="a591a-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a591a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a591a-115">-DefaultProfile</span></span>
<span data-ttu-id="a591a-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a591a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a591a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a591a-117">-PassThru</span></span>
<span data-ttu-id="a591a-118">passthru</span><span class="sxs-lookup"><span data-stu-id="a591a-118">passthru</span></span>

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

### <span data-ttu-id="a591a-119">-확인</span><span class="sxs-lookup"><span data-stu-id="a591a-119">-Confirm</span></span>
<span data-ttu-id="a591a-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a591a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a591a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a591a-121">-WhatIf</span></span>
<span data-ttu-id="a591a-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a591a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a591a-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a591a-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a591a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a591a-124">CommonParameters</span></span>
<span data-ttu-id="a591a-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a591a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a591a-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a591a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a591a-127">입력</span><span class="sxs-lookup"><span data-stu-id="a591a-127">INPUTS</span></span>

### <span data-ttu-id="a591a-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a591a-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a591a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a591a-129">System.String</span></span>

### <span data-ttu-id="a591a-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a591a-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a591a-131">출력</span><span class="sxs-lookup"><span data-stu-id="a591a-131">OUTPUTS</span></span>

### <span data-ttu-id="a591a-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a591a-132">System.Boolean</span></span>

## <span data-ttu-id="a591a-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a591a-133">NOTES</span></span>

## <span data-ttu-id="a591a-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a591a-134">RELATED LINKS</span></span>

[<span data-ttu-id="a591a-135">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a591a-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="a591a-136">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a591a-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="a591a-137">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a591a-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="a591a-138">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a591a-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="a591a-139">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a591a-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


