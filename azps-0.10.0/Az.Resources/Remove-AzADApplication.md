---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: 956fcf09006e8e65d029bb5e380abc5de0e15c17
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399926"
---
# <span data-ttu-id="17961-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="17961-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="17961-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17961-102">SYNOPSIS</span></span>
<span data-ttu-id="17961-103">Azure Active Directory 애플리케이션을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="17961-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="17961-104">구문</span><span class="sxs-lookup"><span data-stu-id="17961-104">SYNTAX</span></span>

### <span data-ttu-id="17961-105">ObjectIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="17961-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17961-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="17961-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17961-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="17961-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17961-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17961-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17961-109">설명</span><span class="sxs-lookup"><span data-stu-id="17961-109">DESCRIPTION</span></span>
<span data-ttu-id="17961-110">Azure Active Directory 애플리케이션을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="17961-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="17961-111">예제</span><span class="sxs-lookup"><span data-stu-id="17961-111">EXAMPLES</span></span>

### <span data-ttu-id="17961-112">예제 1 - 개체 ID로 애플리케이션 제거</span><span class="sxs-lookup"><span data-stu-id="17961-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="17961-113">테넌트에서 개체 ID가 'b4cd1619-80b3-4cfb-9f8f-9f2333425738'인 애플리케이션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="17961-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="17961-114">예제 2 - 애플리케이션 ID로 애플리케이션 제거</span><span class="sxs-lookup"><span data-stu-id="17961-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="17961-115">테넌트에서 애플리케이션 ID가 'f9c5ea4f-28f0-401a-a491-491a037fa346'인 애플리케이션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="17961-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="17961-116">예제 3 - 파이핑을 사용하여 애플리케이션 제거</span><span class="sxs-lookup"><span data-stu-id="17961-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="17961-117">개체 ID가 'b4cd1619-80b3-4cfb-9f8f-9f2333425738'인 애플리케이션을 Remove-AzADApplication cmdlet에 파이프하여 테넌트에서 애플리케이션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="17961-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="17961-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17961-118">PARAMETERS</span></span>

### <span data-ttu-id="17961-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="17961-119">-ApplicationId</span></span>
<span data-ttu-id="17961-120">제거할 애플리케이션의 애플리케이션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="17961-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="17961-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17961-121">-DefaultProfile</span></span>
<span data-ttu-id="17961-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="17961-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17961-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="17961-123">-DisplayName</span></span>
<span data-ttu-id="17961-124">애플리케이션의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17961-124">The display name of the application.</span></span>

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

### <span data-ttu-id="17961-125">-Force</span><span class="sxs-lookup"><span data-stu-id="17961-125">-Force</span></span>
<span data-ttu-id="17961-126">확인 없이 애플리케이션을 삭제하려면 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="17961-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="17961-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17961-127">-InputObject</span></span>
<span data-ttu-id="17961-128">제거할 애플리케이션을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="17961-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17961-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="17961-129">-ObjectId</span></span>
<span data-ttu-id="17961-130">삭제할 애플리케이션의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="17961-130">The object id of the application to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17961-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17961-131">-PassThru</span></span>
<span data-ttu-id="17961-132">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="17961-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="17961-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17961-133">-Confirm</span></span>
<span data-ttu-id="17961-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="17961-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17961-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17961-135">-WhatIf</span></span>
<span data-ttu-id="17961-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="17961-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17961-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17961-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17961-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17961-138">CommonParameters</span></span>
<span data-ttu-id="17961-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="17961-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17961-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="17961-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17961-141">입력</span><span class="sxs-lookup"><span data-stu-id="17961-141">INPUTS</span></span>

### <span data-ttu-id="17961-142">System.Guid</span><span class="sxs-lookup"><span data-stu-id="17961-142">System.Guid</span></span>

### <span data-ttu-id="17961-143">System.String</span><span class="sxs-lookup"><span data-stu-id="17961-143">System.String</span></span>

### <span data-ttu-id="17961-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="17961-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="17961-145">매개 변수: InputObject(ByValue)</span><span class="sxs-lookup"><span data-stu-id="17961-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="17961-146">출력</span><span class="sxs-lookup"><span data-stu-id="17961-146">OUTPUTS</span></span>

### <span data-ttu-id="17961-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="17961-147">System.Boolean</span></span>

## <span data-ttu-id="17961-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="17961-148">NOTES</span></span>
<span data-ttu-id="17961-149">키워드: azure, Az, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포</span><span class="sxs-lookup"><span data-stu-id="17961-149">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="17961-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17961-150">RELATED LINKS</span></span>

[<span data-ttu-id="17961-151">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="17961-151">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="17961-152">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="17961-152">Get-AzADApplication</span></span>](./Get-AzADApplication.md)


[<span data-ttu-id="17961-153">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="17961-153">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

