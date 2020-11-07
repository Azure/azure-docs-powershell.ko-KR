---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
ms.openlocfilehash: 1861b048a1782f8962708ae5ed2bbd16ebc178b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702197"
---
# <span data-ttu-id="f967d-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="f967d-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="f967d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f967d-102">SYNOPSIS</span></span>
<span data-ttu-id="f967d-103">리소스에 대 한 작업을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f967d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f967d-104">SYNTAX</span></span>

### <span data-ttu-id="f967d-105">리소스 Id입니다. (기본값)</span><span class="sxs-lookup"><span data-stu-id="f967d-105">The resource Id. (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f967d-106">구독 수준에 있는 리소스</span><span class="sxs-lookup"><span data-stu-id="f967d-106">Resource that resides at the subscription level.</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f967d-107">테 넌 트 수준에 있는 리소스</span><span class="sxs-lookup"><span data-stu-id="f967d-107">Resource that resides at the tenant level.</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f967d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f967d-108">DESCRIPTION</span></span>
<span data-ttu-id="f967d-109">**AzureRmResourceAction** cmdlet은 지정 된 Azure 리소스에 대해 작업을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>

<span data-ttu-id="f967d-110">지원 되는 작업 목록을 보려면 Azure 리소스 탐색기 도구를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="f967d-111">예제의</span><span class="sxs-lookup"><span data-stu-id="f967d-111">EXAMPLES</span></span>

## <span data-ttu-id="f967d-112">변수</span><span class="sxs-lookup"><span data-stu-id="f967d-112">PARAMETERS</span></span>

### <span data-ttu-id="f967d-113">-작업</span><span class="sxs-lookup"><span data-stu-id="f967d-113">-Action</span></span>
<span data-ttu-id="f967d-114">호출할 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-114">Specifies the name of the action to invoke.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f967d-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f967d-115">-ApiVersion</span></span>
<span data-ttu-id="f967d-116">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f967d-117">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f967d-118">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="f967d-118">-ExtensionResourceName</span></span>
<span data-ttu-id="f967d-119">이 cmdlet이 작업을 호출 하는 리소스에 대 한 확장 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-119">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="f967d-120">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-120">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="f967d-121">서버 이름 `/` 데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="f967d-121">server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f967d-122">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="f967d-122">-ExtensionResourceType</span></span>
<span data-ttu-id="f967d-123">확장 리소스의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-123">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="f967d-124">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-124">For instance:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f967d-125">-Force</span><span class="sxs-lookup"><span data-stu-id="f967d-125">-Force</span></span>
<span data-ttu-id="f967d-126">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f967d-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f967d-127">-InformationAction</span></span>
<span data-ttu-id="f967d-128">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f967d-129">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f967d-130">하기로</span><span class="sxs-lookup"><span data-stu-id="f967d-130">Continue</span></span>
- <span data-ttu-id="f967d-131">숨기기</span><span class="sxs-lookup"><span data-stu-id="f967d-131">Ignore</span></span>
- <span data-ttu-id="f967d-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="f967d-132">Inquire</span></span>
- <span data-ttu-id="f967d-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f967d-133">SilentlyContinue</span></span>
- <span data-ttu-id="f967d-134">중지가</span><span class="sxs-lookup"><span data-stu-id="f967d-134">Stop</span></span>
- <span data-ttu-id="f967d-135">대기</span><span class="sxs-lookup"><span data-stu-id="f967d-135">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f967d-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f967d-136">-InformationVariable</span></span>
<span data-ttu-id="f967d-137">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-137">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f967d-138">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="f967d-138">-ODataQuery</span></span>
<span data-ttu-id="f967d-139">OData (Open Data Protocol) 스타일 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-139">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="f967d-140">이 cmdlet은이 값을 다른 모든 필터 외에도 요청에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-140">This cmdlet appends this value to the request in addition to any other filters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f967d-141">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="f967d-141">-Parameters</span></span>
<span data-ttu-id="f967d-142">이 cmdlet이 호출 하는 작업에 대 한 매개 변수를 해시 테이블로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-142">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f967d-143">-Pre</span><span class="sxs-lookup"><span data-stu-id="f967d-143">-Pre</span></span>
<span data-ttu-id="f967d-144">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f967d-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f967d-145">-ResourceGroupName</span></span>
<span data-ttu-id="f967d-146">이 cmdlet이 동작을 호출 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-146">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f967d-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f967d-147">-ResourceId</span></span>
<span data-ttu-id="f967d-148">이 cmdlet이 작업을 호출 하는 리소스의 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-148">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="f967d-149">ID에는 다음 예제와 같이 구독이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-149">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="f967d-150">`/subscriptions/`구독 ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="f967d-150">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: The resource Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f967d-151">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="f967d-151">-ResourceName</span></span>
<span data-ttu-id="f967d-152">이 cmdlet이 작업을 호출 하는 리소스의 리소스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-152">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="f967d-153">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-153">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f967d-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f967d-154">-ResourceType</span></span>
<span data-ttu-id="f967d-155">리소스의 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="f967d-156">예를 들어 데이터베이스의 경우 리소스 종류는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-156">For instance, for a database, the resource type is as follows:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f967d-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="f967d-157">-TenantLevel</span></span>
<span data-ttu-id="f967d-158">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-158">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f967d-159">-확인</span><span class="sxs-lookup"><span data-stu-id="f967d-159">-Confirm</span></span>
<span data-ttu-id="f967d-160">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f967d-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f967d-161">-WhatIf</span></span>
<span data-ttu-id="f967d-162">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f967d-163">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f967d-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f967d-164">-DefaultProfile</span></span>
<span data-ttu-id="f967d-165">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f967d-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f967d-166">CommonParameters</span></span>
<span data-ttu-id="f967d-167">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f967d-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f967d-168">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f967d-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f967d-169">입력</span><span class="sxs-lookup"><span data-stu-id="f967d-169">INPUTS</span></span>

## <span data-ttu-id="f967d-170">출력</span><span class="sxs-lookup"><span data-stu-id="f967d-170">OUTPUTS</span></span>

### <span data-ttu-id="f967d-171">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="f967d-171">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f967d-172">상속자</span><span class="sxs-lookup"><span data-stu-id="f967d-172">NOTES</span></span>

## <span data-ttu-id="f967d-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f967d-173">RELATED LINKS</span></span>

