---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
ms.openlocfilehash: 3101f58720130a6e5f7c91fb4489d96915d8c4e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957824"
---
# <span data-ttu-id="4addf-101">Remove-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="4addf-101">Remove-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="4addf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4addf-102">SYNOPSIS</span></span>
<span data-ttu-id="4addf-103">값이라는 API Management를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4addf-103">Removes an API Management Named Value.</span></span>

## <span data-ttu-id="4addf-104">구문</span><span class="sxs-lookup"><span data-stu-id="4addf-104">SYNTAX</span></span>

```
Remove-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4addf-105">설명</span><span class="sxs-lookup"><span data-stu-id="4addf-105">DESCRIPTION</span></span>
<span data-ttu-id="4addf-106">**Remove-AzApiManagementNamedValue** cmdlet은 값이라는 Azure API **Management를 제거합니다.**</span><span class="sxs-lookup"><span data-stu-id="4addf-106">The **Remove-AzApiManagementNamedValue** cmdlet removes an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="4addf-107">예제</span><span class="sxs-lookup"><span data-stu-id="4addf-107">EXAMPLES</span></span>

### <span data-ttu-id="4addf-108">예제 1: 명명된 값 제거</span><span class="sxs-lookup"><span data-stu-id="4addf-108">Example 1: Remove the named value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -PassThru
```

<span data-ttu-id="4addf-109">이 명령은 ID 속성11이 있는 명명된 값을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4addf-109">This command removes the named value that has the ID Property11.</span></span>

## <span data-ttu-id="4addf-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4addf-110">PARAMETERS</span></span>

### <span data-ttu-id="4addf-111">-Context</span><span class="sxs-lookup"><span data-stu-id="4addf-111">-Context</span></span>
<span data-ttu-id="4addf-112">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="4addf-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4addf-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="4addf-113">This parameter is required.</span></span>

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

### <span data-ttu-id="4addf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4addf-114">-DefaultProfile</span></span>
<span data-ttu-id="4addf-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4addf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4addf-116">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="4addf-116">-NamedValueId</span></span>
<span data-ttu-id="4addf-117">기존 명명된 값의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4addf-117">Identifier of existing named value.</span></span>
<span data-ttu-id="4addf-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="4addf-118">This parameter is required.</span></span>

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

### <span data-ttu-id="4addf-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4addf-119">-PassThru</span></span>
<span data-ttu-id="4addf-120">지정한 경우 작업이 성공할 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="4addf-120">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="4addf-121">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="4addf-121">This parameter is optional.</span></span>
<span data-ttu-id="4addf-122">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="4addf-122">Default value is false.</span></span>

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

### <span data-ttu-id="4addf-123">-확인</span><span class="sxs-lookup"><span data-stu-id="4addf-123">-Confirm</span></span>
<span data-ttu-id="4addf-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4addf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4addf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4addf-125">-WhatIf</span></span>
<span data-ttu-id="4addf-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4addf-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4addf-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4addf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4addf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4addf-128">CommonParameters</span></span>
<span data-ttu-id="4addf-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4addf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4addf-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4addf-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4addf-131">입력</span><span class="sxs-lookup"><span data-stu-id="4addf-131">INPUTS</span></span>

### <span data-ttu-id="4addf-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4addf-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4addf-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4addf-133">System.String</span></span>

### <span data-ttu-id="4addf-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4addf-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4addf-135">출력</span><span class="sxs-lookup"><span data-stu-id="4addf-135">OUTPUTS</span></span>

### <span data-ttu-id="4addf-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4addf-136">System.Boolean</span></span>

## <span data-ttu-id="4addf-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4addf-137">NOTES</span></span>

## <span data-ttu-id="4addf-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4addf-138">RELATED LINKS</span></span>
