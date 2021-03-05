---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
ms.openlocfilehash: 4ddeee0b0efbb55d98e8e14be1bc84ea83b38e6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963323"
---
# <span data-ttu-id="90515-101">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="90515-101">Remove-AzApiManagementGroup</span></span>

## <span data-ttu-id="90515-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90515-102">SYNOPSIS</span></span>
<span data-ttu-id="90515-103">기존 API 관리 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="90515-103">Removes an existing API management group.</span></span>

## <span data-ttu-id="90515-104">구문</span><span class="sxs-lookup"><span data-stu-id="90515-104">SYNTAX</span></span>

```
Remove-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90515-105">설명</span><span class="sxs-lookup"><span data-stu-id="90515-105">DESCRIPTION</span></span>
<span data-ttu-id="90515-106">**Remove-AzApiManagementGroup** cmdlet은 기존 API 관리 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="90515-106">The **Remove-AzApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="90515-107">예제</span><span class="sxs-lookup"><span data-stu-id="90515-107">EXAMPLES</span></span>

### <span data-ttu-id="90515-108">예제 1: 기존 관리 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="90515-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="90515-109">이 명령은 Group0001이라는 기존 관리 그룹을 제거하고 사용자에게 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90515-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="90515-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="90515-110">PARAMETERS</span></span>

### <span data-ttu-id="90515-111">-Context</span><span class="sxs-lookup"><span data-stu-id="90515-111">-Context</span></span>
<span data-ttu-id="90515-112">**PsApiManagementContext** 개체의 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90515-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="90515-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90515-113">-DefaultProfile</span></span>
<span data-ttu-id="90515-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90515-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90515-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="90515-115">-GroupId</span></span>
<span data-ttu-id="90515-116">관리 그룹의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90515-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="90515-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90515-117">-PassThru</span></span>
<span data-ttu-id="90515-118">이 cmdlet은 성공하는 경우 $True 값을 반환하거나, 그렇지 않은 경우 $False 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="90515-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="90515-119">-확인</span><span class="sxs-lookup"><span data-stu-id="90515-119">-Confirm</span></span>
<span data-ttu-id="90515-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="90515-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90515-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90515-121">-WhatIf</span></span>
<span data-ttu-id="90515-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="90515-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90515-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90515-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90515-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90515-124">CommonParameters</span></span>
<span data-ttu-id="90515-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="90515-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90515-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90515-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90515-127">입력</span><span class="sxs-lookup"><span data-stu-id="90515-127">INPUTS</span></span>

### <span data-ttu-id="90515-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="90515-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="90515-129">System.String</span><span class="sxs-lookup"><span data-stu-id="90515-129">System.String</span></span>

### <span data-ttu-id="90515-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="90515-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="90515-131">출력</span><span class="sxs-lookup"><span data-stu-id="90515-131">OUTPUTS</span></span>

### <span data-ttu-id="90515-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="90515-132">System.Boolean</span></span>

## <span data-ttu-id="90515-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="90515-133">NOTES</span></span>

## <span data-ttu-id="90515-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90515-134">RELATED LINKS</span></span>

[<span data-ttu-id="90515-135">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="90515-135">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="90515-136">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="90515-136">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="90515-137">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="90515-137">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


