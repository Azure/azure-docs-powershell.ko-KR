---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: be060c320c05b44a4b0d8f79b519f63e4dd47bcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996151"
---
# <span data-ttu-id="149ba-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="149ba-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="149ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="149ba-102">SYNOPSIS</span></span>
<span data-ttu-id="149ba-103">개인 엔드포인트 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="149ba-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="149ba-104">구문</span><span class="sxs-lookup"><span data-stu-id="149ba-104">SYNTAX</span></span>

### <span data-ttu-id="149ba-105">ByResourceId(기본값)</span><span class="sxs-lookup"><span data-stu-id="149ba-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection -ResourceId <String>
 [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="149ba-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="149ba-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="149ba-107">설명</span><span class="sxs-lookup"><span data-stu-id="149ba-107">DESCRIPTION</span></span>
<span data-ttu-id="149ba-108">**Remove-AzPrivateEndpointConnection** cmdlet은 개인 엔드포인트 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="149ba-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span>

## <span data-ttu-id="149ba-109">예제</span><span class="sxs-lookup"><span data-stu-id="149ba-109">EXAMPLES</span></span>

### <span data-ttu-id="149ba-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="149ba-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="149ba-111">이 예제에서는 MyPrivateEndpointConnection1이라는 개인 엔드포인트 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="149ba-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="149ba-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="149ba-112">PARAMETERS</span></span>

### <span data-ttu-id="149ba-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="149ba-113">-AsJob</span></span>
<span data-ttu-id="149ba-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="149ba-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="149ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="149ba-115">-DefaultProfile</span></span>
<span data-ttu-id="149ba-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="149ba-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="149ba-117">-Force</span><span class="sxs-lookup"><span data-stu-id="149ba-117">-Force</span></span>
<span data-ttu-id="149ba-118">리소스를 삭제하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="149ba-118">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="149ba-119">-Name</span><span class="sxs-lookup"><span data-stu-id="149ba-119">-Name</span></span>
<span data-ttu-id="149ba-120">개인 엔드포인트 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="149ba-120">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="149ba-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="149ba-121">-PassThru</span></span>
<span data-ttu-id="149ba-122">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="149ba-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="149ba-123">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="149ba-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="149ba-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="149ba-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="149ba-125">개인 링크 리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="149ba-125">The private link resource type.</span></span>

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

### <span data-ttu-id="149ba-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="149ba-126">-ResourceGroupName</span></span>
<span data-ttu-id="149ba-127">개인 엔드포인트 연결의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="149ba-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="149ba-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="149ba-128">-ResourceId</span></span>
<span data-ttu-id="149ba-129">개인 엔드포인트 연결의 Azure 리소스 관리자 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="149ba-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="149ba-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="149ba-130">-ServiceName</span></span>
<span data-ttu-id="149ba-131">개인 엔드포인트 연결이 속한 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="149ba-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="149ba-132">-확인</span><span class="sxs-lookup"><span data-stu-id="149ba-132">-Confirm</span></span>
<span data-ttu-id="149ba-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="149ba-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="149ba-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="149ba-134">-WhatIf</span></span>
<span data-ttu-id="149ba-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="149ba-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="149ba-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="149ba-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="149ba-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="149ba-137">CommonParameters</span></span>
<span data-ttu-id="149ba-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="149ba-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="149ba-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="149ba-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="149ba-140">입력</span><span class="sxs-lookup"><span data-stu-id="149ba-140">INPUTS</span></span>

### <span data-ttu-id="149ba-141">System.String</span><span class="sxs-lookup"><span data-stu-id="149ba-141">System.String</span></span>

## <span data-ttu-id="149ba-142">출력</span><span class="sxs-lookup"><span data-stu-id="149ba-142">OUTPUTS</span></span>

### <span data-ttu-id="149ba-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="149ba-143">System.Boolean</span></span>

## <span data-ttu-id="149ba-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="149ba-144">NOTES</span></span>

## <span data-ttu-id="149ba-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="149ba-145">RELATED LINKS</span></span>

[<span data-ttu-id="149ba-146">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="149ba-146">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="149ba-147">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="149ba-147">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="149ba-148">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="149ba-148">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="149ba-149">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="149ba-149">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
