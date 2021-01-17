---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: ffca6c1bc32d809f7bbb93c3b76dd9490f9fafb8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382152"
---
# <span data-ttu-id="3984b-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="3984b-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="3984b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3984b-102">SYNOPSIS</span></span>
<span data-ttu-id="3984b-103">캐시 엔터티를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3984b-103">Removes the cache entity.</span></span>

## <span data-ttu-id="3984b-104">구문</span><span class="sxs-lookup"><span data-stu-id="3984b-104">SYNTAX</span></span>

### <span data-ttu-id="3984b-105">ContextParameterSetName(기본값)</span><span class="sxs-lookup"><span data-stu-id="3984b-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3984b-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3984b-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3984b-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3984b-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3984b-108">설명</span><span class="sxs-lookup"><span data-stu-id="3984b-108">DESCRIPTION</span></span>
<span data-ttu-id="3984b-109">**Remove-AzApiManagementCache** cmdlet은 캐시 엔터티를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3984b-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="3984b-110">예제</span><span class="sxs-lookup"><span data-stu-id="3984b-110">EXAMPLES</span></span>

### <span data-ttu-id="3984b-111">예제 1: 캐시 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="3984b-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="3984b-112">이 cmdlet은 `centralus` Api Management 서비스에서 캐시를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3984b-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="3984b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3984b-113">PARAMETERS</span></span>

### <span data-ttu-id="3984b-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="3984b-114">-CacheId</span></span>
<span data-ttu-id="3984b-115">기존 cacheId의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="3984b-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="3984b-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="3984b-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3984b-117">-Context</span><span class="sxs-lookup"><span data-stu-id="3984b-117">-Context</span></span>
<span data-ttu-id="3984b-118">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="3984b-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3984b-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="3984b-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3984b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3984b-120">-DefaultProfile</span></span>
<span data-ttu-id="3984b-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3984b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3984b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3984b-122">-InputObject</span></span>
<span data-ttu-id="3984b-123">PsApiManagementCache의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="3984b-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="3984b-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="3984b-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3984b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3984b-125">-PassThru</span></span>
<span data-ttu-id="3984b-126">지정된 경우 작업이 성공하는 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="3984b-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="3984b-127">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="3984b-127">This parameter is optional.</span></span>
<span data-ttu-id="3984b-128">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="3984b-128">Default value is false.</span></span>

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

### <span data-ttu-id="3984b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3984b-129">-ResourceId</span></span>
<span data-ttu-id="3984b-130">캐시의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="3984b-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="3984b-131">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="3984b-131">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3984b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3984b-132">-Confirm</span></span>
<span data-ttu-id="3984b-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3984b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3984b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3984b-134">-WhatIf</span></span>
<span data-ttu-id="3984b-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3984b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3984b-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3984b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3984b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3984b-137">CommonParameters</span></span>
<span data-ttu-id="3984b-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3984b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3984b-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3984b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3984b-140">입력</span><span class="sxs-lookup"><span data-stu-id="3984b-140">INPUTS</span></span>

### <span data-ttu-id="3984b-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3984b-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3984b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3984b-142">System.String</span></span>

### <span data-ttu-id="3984b-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3984b-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3984b-144">출력</span><span class="sxs-lookup"><span data-stu-id="3984b-144">OUTPUTS</span></span>

### <span data-ttu-id="3984b-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3984b-145">System.Boolean</span></span>

## <span data-ttu-id="3984b-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3984b-146">NOTES</span></span>

## <span data-ttu-id="3984b-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3984b-147">RELATED LINKS</span></span>

[<span data-ttu-id="3984b-148">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="3984b-148">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="3984b-149">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="3984b-149">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="3984b-150">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="3984b-150">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
