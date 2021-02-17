---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: 13f5297efc19aa56cc5af55962c072f5ff2a32d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210360"
---
# <span data-ttu-id="10414-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="10414-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="10414-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10414-102">SYNOPSIS</span></span>
<span data-ttu-id="10414-103">API를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="10414-103">Removes an API.</span></span>

## <span data-ttu-id="10414-104">구문</span><span class="sxs-lookup"><span data-stu-id="10414-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10414-105">설명</span><span class="sxs-lookup"><span data-stu-id="10414-105">DESCRIPTION</span></span>
<span data-ttu-id="10414-106">**Remove-AzApiManagementApi** cmdlet은 기존 API를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="10414-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="10414-107">예제</span><span class="sxs-lookup"><span data-stu-id="10414-107">EXAMPLES</span></span>

### <span data-ttu-id="10414-108">예제 1: API 제거</span><span class="sxs-lookup"><span data-stu-id="10414-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="10414-109">이 명령은 지정된 ID로 API를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="10414-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="10414-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10414-110">PARAMETERS</span></span>

### <span data-ttu-id="10414-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="10414-111">-ApiId</span></span>
<span data-ttu-id="10414-112">API 제거의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="10414-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="10414-113">-Context</span><span class="sxs-lookup"><span data-stu-id="10414-113">-Context</span></span>
<span data-ttu-id="10414-114">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="10414-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="10414-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10414-115">-DefaultProfile</span></span>
<span data-ttu-id="10414-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="10414-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10414-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10414-117">-PassThru</span></span>
<span data-ttu-id="10414-118">passthru</span><span class="sxs-lookup"><span data-stu-id="10414-118">passthru</span></span>

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

### <span data-ttu-id="10414-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10414-119">-Confirm</span></span>
<span data-ttu-id="10414-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="10414-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10414-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10414-121">-WhatIf</span></span>
<span data-ttu-id="10414-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="10414-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10414-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10414-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10414-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10414-124">CommonParameters</span></span>
<span data-ttu-id="10414-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="10414-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10414-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="10414-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10414-127">입력</span><span class="sxs-lookup"><span data-stu-id="10414-127">INPUTS</span></span>

### <span data-ttu-id="10414-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="10414-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="10414-129">System.String</span><span class="sxs-lookup"><span data-stu-id="10414-129">System.String</span></span>

### <span data-ttu-id="10414-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="10414-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="10414-131">출력</span><span class="sxs-lookup"><span data-stu-id="10414-131">OUTPUTS</span></span>

### <span data-ttu-id="10414-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="10414-132">System.Boolean</span></span>

## <span data-ttu-id="10414-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="10414-133">NOTES</span></span>

## <span data-ttu-id="10414-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10414-134">RELATED LINKS</span></span>

[<span data-ttu-id="10414-135">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="10414-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="10414-136">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="10414-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="10414-137">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="10414-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="10414-138">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="10414-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="10414-139">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="10414-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


