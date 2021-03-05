---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: d4415b2f97cb92c8694c0ca56a3b47d751a065f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986645"
---
# <span data-ttu-id="d8289-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d8289-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="d8289-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8289-102">SYNOPSIS</span></span>
<span data-ttu-id="d8289-103">Azure Active Directory 애플리케이션을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d8289-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="d8289-104">구문</span><span class="sxs-lookup"><span data-stu-id="d8289-104">SYNTAX</span></span>

### <span data-ttu-id="d8289-105">ObjectIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d8289-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8289-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8289-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8289-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8289-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8289-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8289-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8289-109">설명</span><span class="sxs-lookup"><span data-stu-id="d8289-109">DESCRIPTION</span></span>
<span data-ttu-id="d8289-110">Azure Active Directory 애플리케이션을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d8289-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="d8289-111">예제</span><span class="sxs-lookup"><span data-stu-id="d8289-111">EXAMPLES</span></span>

### <span data-ttu-id="d8289-112">예제 1: 개체 ID로 애플리케이션 제거</span><span class="sxs-lookup"><span data-stu-id="d8289-112">Example 1: Remove application by object id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="d8289-113">테넌트에서 개체 ID 'b4cd1619-80b3-4cfb-9f8f-9f233425738'을 사용하여 애플리케이션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d8289-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="d8289-114">예제 2: 애플리케이션 ID로 애플리케이션 제거</span><span class="sxs-lookup"><span data-stu-id="d8289-114">Example 2: Remove application by application id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="d8289-115">테넌트에서 애플리케이션 ID 'f9c5ea4f-28f0-401a-a491-491a037fa346'을 사용하여 애플리케이션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d8289-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="d8289-116">예제 3: 배관을 사용하여 애플리케이션 제거</span><span class="sxs-lookup"><span data-stu-id="d8289-116">Example 3: Remove application by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="d8289-117">개체 ID 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' 및 테넌트에서 애플리케이션을 제거하기 위해 Remove-AzADApplication cmdlet에 있는 파이프를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d8289-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="d8289-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d8289-118">PARAMETERS</span></span>

### <span data-ttu-id="d8289-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d8289-119">-ApplicationId</span></span>
<span data-ttu-id="d8289-120">제거할 애플리케이션의 애플리케이션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d8289-120">The application id of the application to remove.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8289-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8289-121">-DefaultProfile</span></span>
<span data-ttu-id="d8289-122">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d8289-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8289-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d8289-123">-DisplayName</span></span>
<span data-ttu-id="d8289-124">애플리케이션의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8289-124">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8289-125">-Force</span><span class="sxs-lookup"><span data-stu-id="d8289-125">-Force</span></span>
<span data-ttu-id="d8289-126">확인 없이 애플리케이션을 삭제하려면 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="d8289-126">Switch to delete an application without a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8289-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8289-127">-InputObject</span></span>
<span data-ttu-id="d8289-128">제거할 애플리케이션을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d8289-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8289-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d8289-129">-ObjectId</span></span>
<span data-ttu-id="d8289-130">삭제할 애플리케이션의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d8289-130">The object id of the application to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8289-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8289-131">-PassThru</span></span>
<span data-ttu-id="d8289-132">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8289-132">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8289-133">-확인</span><span class="sxs-lookup"><span data-stu-id="d8289-133">-Confirm</span></span>
<span data-ttu-id="d8289-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8289-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8289-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8289-135">-WhatIf</span></span>
<span data-ttu-id="d8289-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d8289-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8289-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8289-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8289-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8289-138">CommonParameters</span></span>
<span data-ttu-id="d8289-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d8289-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8289-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8289-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8289-141">입력</span><span class="sxs-lookup"><span data-stu-id="d8289-141">INPUTS</span></span>

### <span data-ttu-id="d8289-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d8289-142">System.String</span></span>

### <span data-ttu-id="d8289-143">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d8289-143">System.Guid</span></span>

### <span data-ttu-id="d8289-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="d8289-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="d8289-145">출력</span><span class="sxs-lookup"><span data-stu-id="d8289-145">OUTPUTS</span></span>

### <span data-ttu-id="d8289-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d8289-146">System.Boolean</span></span>

## <span data-ttu-id="d8289-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d8289-147">NOTES</span></span>
<span data-ttu-id="d8289-148">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포</span><span class="sxs-lookup"><span data-stu-id="d8289-148">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d8289-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8289-149">RELATED LINKS</span></span>

[<span data-ttu-id="d8289-150">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d8289-150">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="d8289-151">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d8289-151">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="d8289-152">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d8289-152">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

[<span data-ttu-id="d8289-153">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d8289-153">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

