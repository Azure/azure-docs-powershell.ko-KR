---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 9de25adae04afd0f09a2a09118c55d4e679a44db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871186"
---
# <span data-ttu-id="72566-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="72566-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="72566-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72566-102">SYNOPSIS</span></span>
<span data-ttu-id="72566-103">개인 끝점 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="72566-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="72566-104">구문과</span><span class="sxs-lookup"><span data-stu-id="72566-104">SYNTAX</span></span>

### <span data-ttu-id="72566-105">ByResourceId (기본값)</span><span class="sxs-lookup"><span data-stu-id="72566-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection [-Force] [-AsJob] [-PassThru] -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72566-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="72566-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection [-Force] [-AsJob] [-PassThru] -Name <String> -ServiceName <String>
 -ResourceGroupName <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72566-107">설명은</span><span class="sxs-lookup"><span data-stu-id="72566-107">DESCRIPTION</span></span>
<span data-ttu-id="72566-108">**AzPrivateEndpointConnection** cmdlet은 개인 끝점 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="72566-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span> 

## <span data-ttu-id="72566-109">예제의</span><span class="sxs-lookup"><span data-stu-id="72566-109">EXAMPLES</span></span>

### <span data-ttu-id="72566-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="72566-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="72566-111">이 예제에서는 MyPrivateEndpointConnection1 이라는 개인 끝점 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="72566-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="72566-112">변수</span><span class="sxs-lookup"><span data-stu-id="72566-112">PARAMETERS</span></span>

### <span data-ttu-id="72566-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72566-113">-AsJob</span></span>
<span data-ttu-id="72566-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="72566-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="72566-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72566-115">-DefaultProfile</span></span>
<span data-ttu-id="72566-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="72566-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72566-117">-설명</span><span class="sxs-lookup"><span data-stu-id="72566-117">-Description</span></span>
<span data-ttu-id="72566-118">작업의 이유입니다.</span><span class="sxs-lookup"><span data-stu-id="72566-118">The reason of action.</span></span>

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

### <span data-ttu-id="72566-119">-Force</span><span class="sxs-lookup"><span data-stu-id="72566-119">-Force</span></span>
<span data-ttu-id="72566-120">리소스를 삭제 하려는 경우 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="72566-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="72566-121">-이름</span><span class="sxs-lookup"><span data-stu-id="72566-121">-Name</span></span>
<span data-ttu-id="72566-122">개인 끝점 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="72566-122">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="72566-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72566-123">-PassThru</span></span>
<span data-ttu-id="72566-124">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="72566-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="72566-125">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72566-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="72566-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72566-126">-ResourceGroupName</span></span>
<span data-ttu-id="72566-127">개인 끝점 연결의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="72566-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="72566-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72566-128">-ResourceId</span></span>
<span data-ttu-id="72566-129">개인 끝점 연결의 Azure resource manager id입니다.</span><span class="sxs-lookup"><span data-stu-id="72566-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="72566-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="72566-130">-ServiceName</span></span>
<span data-ttu-id="72566-131">개인 끝점 연결이 있는 개인 링크 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="72566-131">The name of the private link service that has the private endpoint connection.</span></span>

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

### <span data-ttu-id="72566-132">-확인</span><span class="sxs-lookup"><span data-stu-id="72566-132">-Confirm</span></span>
<span data-ttu-id="72566-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="72566-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72566-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72566-134">-WhatIf</span></span>
<span data-ttu-id="72566-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="72566-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72566-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72566-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72566-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72566-137">CommonParameters</span></span>
<span data-ttu-id="72566-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="72566-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72566-139">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="72566-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72566-140">입력</span><span class="sxs-lookup"><span data-stu-id="72566-140">INPUTS</span></span>

### <span data-ttu-id="72566-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="72566-141">System.String</span></span>

## <span data-ttu-id="72566-142">출력</span><span class="sxs-lookup"><span data-stu-id="72566-142">OUTPUTS</span></span>

### <span data-ttu-id="72566-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="72566-143">System.Boolean</span></span>

## <span data-ttu-id="72566-144">상속자</span><span class="sxs-lookup"><span data-stu-id="72566-144">NOTES</span></span>

## <span data-ttu-id="72566-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="72566-145">RELATED LINKS</span></span>

[<span data-ttu-id="72566-146">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="72566-146">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
