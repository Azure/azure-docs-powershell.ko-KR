---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
ms.openlocfilehash: c2cf7f46a7f7f73443a9d7d2b06dbfde943b28d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199729"
---
# <span data-ttu-id="94532-101">Remove-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="94532-101">Remove-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="94532-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94532-102">SYNOPSIS</span></span>
<span data-ttu-id="94532-103">API Management 명명된 값을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="94532-103">Removes an API Management Named Value.</span></span>

## <span data-ttu-id="94532-104">구문</span><span class="sxs-lookup"><span data-stu-id="94532-104">SYNTAX</span></span>

```
Remove-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94532-105">설명</span><span class="sxs-lookup"><span data-stu-id="94532-105">DESCRIPTION</span></span>
<span data-ttu-id="94532-106">**Remove-AzApiManagementNamedValue** cmdlet은 Azure API Management 명명된 **값을 제거합니다.**</span><span class="sxs-lookup"><span data-stu-id="94532-106">The **Remove-AzApiManagementNamedValue** cmdlet removes an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="94532-107">예제</span><span class="sxs-lookup"><span data-stu-id="94532-107">EXAMPLES</span></span>

### <span data-ttu-id="94532-108">예제 1: 명명된 값 제거</span><span class="sxs-lookup"><span data-stu-id="94532-108">Example 1: Remove the named value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -PassThru
```

<span data-ttu-id="94532-109">이 명령은 ID Property11이 있는 명명된 값을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="94532-109">This command removes the named value that has the ID Property11.</span></span>

## <span data-ttu-id="94532-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94532-110">PARAMETERS</span></span>

### <span data-ttu-id="94532-111">-Context</span><span class="sxs-lookup"><span data-stu-id="94532-111">-Context</span></span>
<span data-ttu-id="94532-112">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="94532-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="94532-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="94532-113">This parameter is required.</span></span>

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

### <span data-ttu-id="94532-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94532-114">-DefaultProfile</span></span>
<span data-ttu-id="94532-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94532-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94532-116">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="94532-116">-NamedValueId</span></span>
<span data-ttu-id="94532-117">기존 명명된 값의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="94532-117">Identifier of existing named value.</span></span>
<span data-ttu-id="94532-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="94532-118">This parameter is required.</span></span>

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

### <span data-ttu-id="94532-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94532-119">-PassThru</span></span>
<span data-ttu-id="94532-120">지정된 경우 작업이 성공하는 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="94532-120">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="94532-121">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="94532-121">This parameter is optional.</span></span>
<span data-ttu-id="94532-122">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="94532-122">Default value is false.</span></span>

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

### <span data-ttu-id="94532-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94532-123">-Confirm</span></span>
<span data-ttu-id="94532-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="94532-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94532-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94532-125">-WhatIf</span></span>
<span data-ttu-id="94532-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="94532-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94532-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94532-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94532-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94532-128">CommonParameters</span></span>
<span data-ttu-id="94532-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="94532-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94532-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="94532-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94532-131">입력</span><span class="sxs-lookup"><span data-stu-id="94532-131">INPUTS</span></span>

### <span data-ttu-id="94532-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="94532-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="94532-133">System.String</span><span class="sxs-lookup"><span data-stu-id="94532-133">System.String</span></span>

### <span data-ttu-id="94532-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="94532-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="94532-135">출력</span><span class="sxs-lookup"><span data-stu-id="94532-135">OUTPUTS</span></span>

### <span data-ttu-id="94532-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="94532-136">System.Boolean</span></span>

## <span data-ttu-id="94532-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="94532-137">NOTES</span></span>

## <span data-ttu-id="94532-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94532-138">RELATED LINKS</span></span>
