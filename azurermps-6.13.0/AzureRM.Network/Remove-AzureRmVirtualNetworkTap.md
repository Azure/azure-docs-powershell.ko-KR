---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: 59e3b7f233077c8ed7064bcb1757634fe08c262b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529467"
---
# <span data-ttu-id="efea0-101">Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="efea0-101">Remove-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="efea0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efea0-102">SYNOPSIS</span></span>
<span data-ttu-id="efea0-103">가상 네트워크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="efea0-103">Removes a virtual network tap.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efea0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="efea0-104">SYNTAX</span></span>

### <span data-ttu-id="efea0-105">RemoveByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="efea0-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzureRmVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efea0-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="efea0-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzureRmVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efea0-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="efea0-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzureRmVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efea0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="efea0-108">DESCRIPTION</span></span>
<span data-ttu-id="efea0-109">**AzureRmVirtualNetworkTap** Cmdlet은 Azure 가상 네트워크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="efea0-109">The **Remove-AzureRmVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="efea0-110">예제의</span><span class="sxs-lookup"><span data-stu-id="efea0-110">EXAMPLES</span></span>

### <span data-ttu-id="efea0-111">예제 1: virtuak 네트워크 탭 제거</span><span class="sxs-lookup"><span data-stu-id="efea0-111">Example 1: Remove a virtuak network tap</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="efea0-112">이 명령은 리소스 그룹 ResourceGroup1에서 VirtualNetworkTap1를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="efea0-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="efea0-113">*Force* 매개 변수는 사용 되지 않으므로 사용자에 게이 작업을 확인 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="efea0-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="efea0-114">변수</span><span class="sxs-lookup"><span data-stu-id="efea0-114">PARAMETERS</span></span>

### <span data-ttu-id="efea0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efea0-115">-AsJob</span></span>
<span data-ttu-id="efea0-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="efea0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="efea0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efea0-117">-DefaultProfile</span></span>
<span data-ttu-id="efea0-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="efea0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efea0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="efea0-119">-Force</span></span>
<span data-ttu-id="efea0-120">리소스를 삭제 하려는 경우 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="efea0-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="efea0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efea0-121">-InputObject</span></span>
<span data-ttu-id="efea0-122">VirtualNetworkTap 리소스에 대 한 참조</span><span class="sxs-lookup"><span data-stu-id="efea0-122">Reference to VirtualNetworkTap resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efea0-123">-이름</span><span class="sxs-lookup"><span data-stu-id="efea0-123">-Name</span></span>
<span data-ttu-id="efea0-124">탭의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efea0-124">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efea0-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="efea0-125">-PassThru</span></span>
<span data-ttu-id="efea0-126">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="efea0-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="efea0-127">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="efea0-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="efea0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efea0-128">-ResourceGroupName</span></span>
<span data-ttu-id="efea0-129">가상 네트워크의 리소스 그룹 이름 탭 합니다.</span><span class="sxs-lookup"><span data-stu-id="efea0-129">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efea0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efea0-130">-ResourceId</span></span>
<span data-ttu-id="efea0-131">VirtualNetworkTap resourceId</span><span class="sxs-lookup"><span data-stu-id="efea0-131">VirtualNetworkTap resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efea0-132">-확인</span><span class="sxs-lookup"><span data-stu-id="efea0-132">-Confirm</span></span>
<span data-ttu-id="efea0-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="efea0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efea0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efea0-134">-WhatIf</span></span>
<span data-ttu-id="efea0-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="efea0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efea0-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="efea0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efea0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efea0-137">CommonParameters</span></span>
<span data-ttu-id="efea0-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="efea0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efea0-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efea0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efea0-140">입력</span><span class="sxs-lookup"><span data-stu-id="efea0-140">INPUTS</span></span>

### <span data-ttu-id="efea0-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="efea0-141">System.String</span></span>

## <span data-ttu-id="efea0-142">출력</span><span class="sxs-lookup"><span data-stu-id="efea0-142">OUTPUTS</span></span>

### <span data-ttu-id="efea0-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="efea0-143">System.Boolean</span></span>

## <span data-ttu-id="efea0-144">상속자</span><span class="sxs-lookup"><span data-stu-id="efea0-144">NOTES</span></span>

## <span data-ttu-id="efea0-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="efea0-145">RELATED LINKS</span></span>
