---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: e9e4a8e902b3d71507a9e9d731ceb518825f8aa6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970352"
---
# <span data-ttu-id="c8cbc-101">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c8cbc-101">Remove-AzADServicePrincipal</span></span>

## <span data-ttu-id="c8cbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="c8cbc-103">Azure Active Directory 서비스 주체가 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8cbc-103">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="c8cbc-104">구문</span><span class="sxs-lookup"><span data-stu-id="c8cbc-104">SYNTAX</span></span>

### <span data-ttu-id="c8cbc-105">ObjectIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c8cbc-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADServicePrincipal -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8cbc-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8cbc-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8cbc-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8cbc-107">SPNParameterSet</span></span>
```
Remove-AzADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8cbc-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8cbc-108">DisplayNameParameterSet</span></span>
```
Remove-AzADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8cbc-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8cbc-109">InputObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8cbc-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8cbc-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8cbc-111">설명</span><span class="sxs-lookup"><span data-stu-id="c8cbc-111">DESCRIPTION</span></span>
<span data-ttu-id="c8cbc-112">Azure Active Directory 서비스 주체가 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8cbc-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="c8cbc-113">예제</span><span class="sxs-lookup"><span data-stu-id="c8cbc-113">EXAMPLES</span></span>

### <span data-ttu-id="c8cbc-114">예제 1 - 개체 ID로 서비스 주체 제거</span><span class="sxs-lookup"><span data-stu-id="c8cbc-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="c8cbc-115">개체 ID '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'를 사용하여 서비스 주체가 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8cbc-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="c8cbc-116">예제 2 - 애플리케이션 ID로 서비스 주체 제거</span><span class="sxs-lookup"><span data-stu-id="c8cbc-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="c8cbc-117">애플리케이션 ID '9263469e-d328-4321-8646-3e3e75d20e76'을 사용하여 서비스 주체가 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8cbc-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="c8cbc-118">예제 3 - SPN에서 서비스 주체 제거</span><span class="sxs-lookup"><span data-stu-id="c8cbc-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="c8cbc-119">서비스 주체 이름 "MyServicePrincipal"을 사용하여 서비스 주체 제거</span><span class="sxs-lookup"><span data-stu-id="c8cbc-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="c8cbc-120">예제 4 - 배관을 사용하여 서비스 주체 제거</span><span class="sxs-lookup"><span data-stu-id="c8cbc-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

<span data-ttu-id="c8cbc-121">개체 ID '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' 및 해당 서비스 주체 제거를 위해 Remove-AzADServicePrincipal cmdlet에 있는 파이프를 사용하여 서비스 주체가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8cbc-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="c8cbc-122">예제 5 - 애플리케이션을 피핑하여 서비스 주체 제거</span><span class="sxs-lookup"><span data-stu-id="c8cbc-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

<span data-ttu-id="c8cbc-123">애플리케이션 ID '9263469e-d328-4321-8646-3e3e75d20e76'을 사용하여 애플리케이션을 Remove-AzADServicePrincipal cmdlet에 연결하여 해당 애플리케이션과 연결된 서비스 주체를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c8cbc-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="c8cbc-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c8cbc-124">PARAMETERS</span></span>

### <span data-ttu-id="c8cbc-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c8cbc-125">-ApplicationId</span></span>
<span data-ttu-id="c8cbc-126">서비스 주체 애플리케이션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c8cbc-126">The service principal application id.</span></span>

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

### <span data-ttu-id="c8cbc-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="c8cbc-127">-ApplicationObject</span></span>
<span data-ttu-id="c8cbc-128">서비스 주체가 제거되는 애플리케이션 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c8cbc-128">The application object whose service principal is being removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8cbc-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8cbc-129">-DefaultProfile</span></span>
<span data-ttu-id="c8cbc-130">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c8cbc-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8cbc-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c8cbc-131">-DisplayName</span></span>
<span data-ttu-id="c8cbc-132">서비스 주체의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c8cbc-132">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8cbc-133">-Force</span><span class="sxs-lookup"><span data-stu-id="c8cbc-133">-Force</span></span>
<span data-ttu-id="c8cbc-134">확인 없이 서비스 주체 삭제로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="c8cbc-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="c8cbc-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8cbc-135">-InputObject</span></span>
<span data-ttu-id="c8cbc-136">서비스 주체 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c8cbc-136">The service principal object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8cbc-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c8cbc-137">-ObjectId</span></span>
<span data-ttu-id="c8cbc-138">삭제할 서비스 주체의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c8cbc-138">The object id of the service principal to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8cbc-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8cbc-139">-PassThru</span></span>
<span data-ttu-id="c8cbc-140">지정한 경우 삭제된 서비스 주체가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8cbc-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="c8cbc-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c8cbc-141">-ServicePrincipalName</span></span>
<span data-ttu-id="c8cbc-142">서비스 주체 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c8cbc-142">The service principal name.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8cbc-143">-확인</span><span class="sxs-lookup"><span data-stu-id="c8cbc-143">-Confirm</span></span>
<span data-ttu-id="c8cbc-144">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8cbc-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8cbc-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8cbc-145">-WhatIf</span></span>
<span data-ttu-id="c8cbc-146">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c8cbc-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8cbc-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8cbc-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8cbc-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8cbc-148">CommonParameters</span></span>
<span data-ttu-id="c8cbc-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c8cbc-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8cbc-150">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8cbc-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8cbc-151">입력</span><span class="sxs-lookup"><span data-stu-id="c8cbc-151">INPUTS</span></span>

### <span data-ttu-id="c8cbc-152">System.String</span><span class="sxs-lookup"><span data-stu-id="c8cbc-152">System.String</span></span>

### <span data-ttu-id="c8cbc-153">System.Guid</span><span class="sxs-lookup"><span data-stu-id="c8cbc-153">System.Guid</span></span>

### <span data-ttu-id="c8cbc-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c8cbc-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="c8cbc-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="c8cbc-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="c8cbc-156">출력</span><span class="sxs-lookup"><span data-stu-id="c8cbc-156">OUTPUTS</span></span>

### <span data-ttu-id="c8cbc-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c8cbc-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="c8cbc-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c8cbc-158">NOTES</span></span>
<span data-ttu-id="c8cbc-159">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포</span><span class="sxs-lookup"><span data-stu-id="c8cbc-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="c8cbc-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c8cbc-160">RELATED LINKS</span></span>

[<span data-ttu-id="c8cbc-161">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c8cbc-161">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="c8cbc-162">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c8cbc-162">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="c8cbc-163">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c8cbc-163">Update-AzADServicePrincipal</span></span>](./Update-AzADServicePrincipal.md)

[<span data-ttu-id="c8cbc-164">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c8cbc-164">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="c8cbc-165">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c8cbc-165">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)
