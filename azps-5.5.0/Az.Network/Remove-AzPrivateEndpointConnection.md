---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 2b7b6755b15c5dcaf0442557eb32b563f0c1af6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206584"
---
# <span data-ttu-id="e344a-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e344a-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="e344a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e344a-102">SYNOPSIS</span></span>
<span data-ttu-id="e344a-103">개인 엔드포인트 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e344a-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="e344a-104">구문</span><span class="sxs-lookup"><span data-stu-id="e344a-104">SYNTAX</span></span>

### <span data-ttu-id="e344a-105">ByResourceId(기본값)</span><span class="sxs-lookup"><span data-stu-id="e344a-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection -ResourceId <String>
 [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e344a-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="e344a-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e344a-107">설명</span><span class="sxs-lookup"><span data-stu-id="e344a-107">DESCRIPTION</span></span>
<span data-ttu-id="e344a-108">**Remove-AzPrivateEndpointConnection** cmdlet은 개인 엔드포인트 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e344a-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span>

## <span data-ttu-id="e344a-109">예제</span><span class="sxs-lookup"><span data-stu-id="e344a-109">EXAMPLES</span></span>

### <span data-ttu-id="e344a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e344a-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="e344a-111">이 예제에서는 MyPrivateEndpointConnection1이라는 개인 엔드포인트 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e344a-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="e344a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e344a-112">PARAMETERS</span></span>

### <span data-ttu-id="e344a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e344a-113">-AsJob</span></span>
<span data-ttu-id="e344a-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e344a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e344a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e344a-115">-DefaultProfile</span></span>
<span data-ttu-id="e344a-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e344a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e344a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e344a-117">-Force</span></span>
<span data-ttu-id="e344a-118">리소스를 삭제하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e344a-118">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="e344a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e344a-119">-Name</span></span>
<span data-ttu-id="e344a-120">개인 엔드포인트 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e344a-120">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e344a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e344a-121">-PassThru</span></span>
<span data-ttu-id="e344a-122">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e344a-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e344a-123">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e344a-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e344a-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="e344a-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="e344a-125">개인 링크 리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="e344a-125">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e344a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e344a-126">-ResourceGroupName</span></span>
<span data-ttu-id="e344a-127">개인 엔드포인트 연결의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e344a-127">The resource group name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e344a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e344a-128">-ResourceId</span></span>
<span data-ttu-id="e344a-129">개인 엔드포인트 연결의 Azure Resource Manager ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e344a-129">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e344a-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e344a-130">-ServiceName</span></span>
<span data-ttu-id="e344a-131">개인 엔드포인트 연결이 속한 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e344a-131">The name of service that the private endpoint connection belong to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e344a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e344a-132">-Confirm</span></span>
<span data-ttu-id="e344a-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e344a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e344a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e344a-134">-WhatIf</span></span>
<span data-ttu-id="e344a-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e344a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e344a-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e344a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e344a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e344a-137">CommonParameters</span></span>
<span data-ttu-id="e344a-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e344a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e344a-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e344a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e344a-140">입력</span><span class="sxs-lookup"><span data-stu-id="e344a-140">INPUTS</span></span>

### <span data-ttu-id="e344a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e344a-141">System.String</span></span>

## <span data-ttu-id="e344a-142">출력</span><span class="sxs-lookup"><span data-stu-id="e344a-142">OUTPUTS</span></span>

### <span data-ttu-id="e344a-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e344a-143">System.Boolean</span></span>

## <span data-ttu-id="e344a-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e344a-144">NOTES</span></span>

## <span data-ttu-id="e344a-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e344a-145">RELATED LINKS</span></span>

[<span data-ttu-id="e344a-146">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e344a-146">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="e344a-147">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e344a-147">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="e344a-148">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e344a-148">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="e344a-149">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e344a-149">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
