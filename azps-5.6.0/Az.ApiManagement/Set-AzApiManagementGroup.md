---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: c243cd47300d2b361e37766ab7e2e5bc906cb2ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965419"
---
# <span data-ttu-id="9737b-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9737b-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="9737b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9737b-102">SYNOPSIS</span></span>
<span data-ttu-id="9737b-103">API 관리 그룹을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="9737b-103">Configures an API management group.</span></span>

## <span data-ttu-id="9737b-104">구문</span><span class="sxs-lookup"><span data-stu-id="9737b-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9737b-105">설명</span><span class="sxs-lookup"><span data-stu-id="9737b-105">DESCRIPTION</span></span>
<span data-ttu-id="9737b-106">**Set-AzApiManagementGroup** cmdlet은 API 관리 그룹을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="9737b-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="9737b-107">예제</span><span class="sxs-lookup"><span data-stu-id="9737b-107">EXAMPLES</span></span>

### <span data-ttu-id="9737b-108">예제 1: 관리 그룹 구성</span><span class="sxs-lookup"><span data-stu-id="9737b-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -GroupId "0001" -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="9737b-109">이 명령은 Group0001이라는 관리 그룹을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="9737b-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="9737b-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9737b-110">PARAMETERS</span></span>

### <span data-ttu-id="9737b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="9737b-111">-Context</span></span>
<span data-ttu-id="9737b-112">**PsApiManagementContext** 개체의 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9737b-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9737b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9737b-113">-DefaultProfile</span></span>
<span data-ttu-id="9737b-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9737b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9737b-115">-Description</span><span class="sxs-lookup"><span data-stu-id="9737b-115">-Description</span></span>
<span data-ttu-id="9737b-116">관리 그룹의 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9737b-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="9737b-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="9737b-117">-GroupId</span></span>
<span data-ttu-id="9737b-118">관리 그룹의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9737b-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="9737b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9737b-119">-Name</span></span>
<span data-ttu-id="9737b-120">관리 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9737b-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="9737b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9737b-121">-PassThru</span></span>
<span data-ttu-id="9737b-122">passthru</span><span class="sxs-lookup"><span data-stu-id="9737b-122">passthru</span></span>

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

### <span data-ttu-id="9737b-123">-확인</span><span class="sxs-lookup"><span data-stu-id="9737b-123">-Confirm</span></span>
<span data-ttu-id="9737b-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9737b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9737b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9737b-125">-WhatIf</span></span>
<span data-ttu-id="9737b-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9737b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9737b-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9737b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9737b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9737b-128">CommonParameters</span></span>
<span data-ttu-id="9737b-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9737b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9737b-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9737b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9737b-131">입력</span><span class="sxs-lookup"><span data-stu-id="9737b-131">INPUTS</span></span>

### <span data-ttu-id="9737b-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9737b-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9737b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9737b-133">System.String</span></span>

### <span data-ttu-id="9737b-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9737b-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9737b-135">출력</span><span class="sxs-lookup"><span data-stu-id="9737b-135">OUTPUTS</span></span>

### <span data-ttu-id="9737b-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9737b-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="9737b-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9737b-137">NOTES</span></span>

## <span data-ttu-id="9737b-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9737b-138">RELATED LINKS</span></span>

[<span data-ttu-id="9737b-139">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9737b-139">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="9737b-140">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9737b-140">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="9737b-141">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9737b-141">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


