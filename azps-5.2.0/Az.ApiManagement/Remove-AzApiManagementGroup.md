---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
ms.openlocfilehash: 73e1fbee1dd20a9a30260727f693376346c87f0e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361383"
---
# <span data-ttu-id="3c5b9-101">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3c5b9-101">Remove-AzApiManagementGroup</span></span>

## <span data-ttu-id="3c5b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c5b9-102">SYNOPSIS</span></span>
<span data-ttu-id="3c5b9-103">기존 API 관리 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3c5b9-103">Removes an existing API management group.</span></span>

## <span data-ttu-id="3c5b9-104">구문</span><span class="sxs-lookup"><span data-stu-id="3c5b9-104">SYNTAX</span></span>

```
Remove-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c5b9-105">설명</span><span class="sxs-lookup"><span data-stu-id="3c5b9-105">DESCRIPTION</span></span>
<span data-ttu-id="3c5b9-106">**Remove-AzApiManagementGroup** cmdlet은 기존 API 관리 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3c5b9-106">The **Remove-AzApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="3c5b9-107">예제</span><span class="sxs-lookup"><span data-stu-id="3c5b9-107">EXAMPLES</span></span>

### <span data-ttu-id="3c5b9-108">예제 1: 기존 관리 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="3c5b9-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="3c5b9-109">이 명령은 Group0001이라는 기존 관리 그룹을 제거하고 사용자에게 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3c5b9-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="3c5b9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c5b9-110">PARAMETERS</span></span>

### <span data-ttu-id="3c5b9-111">-Context</span><span class="sxs-lookup"><span data-stu-id="3c5b9-111">-Context</span></span>
<span data-ttu-id="3c5b9-112">**PsApiManagementContext** 개체의 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c5b9-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3c5b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c5b9-113">-DefaultProfile</span></span>
<span data-ttu-id="3c5b9-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3c5b9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c5b9-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="3c5b9-115">-GroupId</span></span>
<span data-ttu-id="3c5b9-116">관리 그룹의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c5b9-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="3c5b9-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c5b9-117">-PassThru</span></span>
<span data-ttu-id="3c5b9-118">이 cmdlet이 성공하는 경우 $True 값이 반환되거나, 그렇지 않으면 $False 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3c5b9-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="3c5b9-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c5b9-119">-Confirm</span></span>
<span data-ttu-id="3c5b9-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c5b9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c5b9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c5b9-121">-WhatIf</span></span>
<span data-ttu-id="3c5b9-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3c5b9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c5b9-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3c5b9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c5b9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c5b9-124">CommonParameters</span></span>
<span data-ttu-id="3c5b9-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3c5b9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c5b9-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3c5b9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c5b9-127">입력</span><span class="sxs-lookup"><span data-stu-id="3c5b9-127">INPUTS</span></span>

### <span data-ttu-id="3c5b9-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3c5b9-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3c5b9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="3c5b9-129">System.String</span></span>

### <span data-ttu-id="3c5b9-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3c5b9-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3c5b9-131">출력</span><span class="sxs-lookup"><span data-stu-id="3c5b9-131">OUTPUTS</span></span>

### <span data-ttu-id="3c5b9-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3c5b9-132">System.Boolean</span></span>

## <span data-ttu-id="3c5b9-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3c5b9-133">NOTES</span></span>

## <span data-ttu-id="3c5b9-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c5b9-134">RELATED LINKS</span></span>

[<span data-ttu-id="3c5b9-135">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3c5b9-135">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="3c5b9-136">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3c5b9-136">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="3c5b9-137">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3c5b9-137">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


