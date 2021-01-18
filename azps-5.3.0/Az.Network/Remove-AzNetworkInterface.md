---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: f4de49bb2e35bf3d392fba06d663800a5bdc44a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492551"
---
# <span data-ttu-id="67263-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="67263-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="67263-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67263-102">SYNOPSIS</span></span>
<span data-ttu-id="67263-103">네트워크 인터페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="67263-103">Removes a network interface.</span></span>

## <span data-ttu-id="67263-104">구문</span><span class="sxs-lookup"><span data-stu-id="67263-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67263-105">설명</span><span class="sxs-lookup"><span data-stu-id="67263-105">DESCRIPTION</span></span>
<span data-ttu-id="67263-106">**Remove-AzNetworkInterface** cmdlet은 Azure 네트워크 인터페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="67263-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="67263-107">예제</span><span class="sxs-lookup"><span data-stu-id="67263-107">EXAMPLES</span></span>

### <span data-ttu-id="67263-108">예제 1: 네트워크 인터페이스 제거</span><span class="sxs-lookup"><span data-stu-id="67263-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="67263-109">이 명령은 리소스 그룹 ResourceGroup1에서 NetworkInterface1 네트워크 인터페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="67263-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="67263-110">Force *매개* 변수가 사용되지 않는 경우 사용자에게 이 작업을 확인하라는 메시지가 표시될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="67263-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="67263-111">예제 2: 네트워크 인터페이스 제거</span><span class="sxs-lookup"><span data-stu-id="67263-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="67263-112">이 명령은 리소스 그룹 ResourceGroup1의 모든 네트워크 인터페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="67263-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="67263-113">Force *매개* 변수가 사용되어 사용자에게 확인 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67263-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="67263-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67263-114">PARAMETERS</span></span>

### <span data-ttu-id="67263-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67263-115">-AsJob</span></span>
<span data-ttu-id="67263-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="67263-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67263-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67263-117">-DefaultProfile</span></span>
<span data-ttu-id="67263-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="67263-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67263-119">-Force</span><span class="sxs-lookup"><span data-stu-id="67263-119">-Force</span></span>
<span data-ttu-id="67263-120">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="67263-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="67263-121">-Name</span><span class="sxs-lookup"><span data-stu-id="67263-121">-Name</span></span>
<span data-ttu-id="67263-122">이 cmdlet이 제거하는 네트워크 인터페이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67263-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67263-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67263-123">-PassThru</span></span>
<span data-ttu-id="67263-124">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="67263-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="67263-125">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67263-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="67263-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67263-126">-ResourceGroupName</span></span>
<span data-ttu-id="67263-127">이 cmdlet에서 제거하는 네트워크 인터페이스를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67263-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="67263-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67263-128">-Confirm</span></span>
<span data-ttu-id="67263-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="67263-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67263-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67263-130">-WhatIf</span></span>
<span data-ttu-id="67263-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="67263-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67263-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67263-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67263-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67263-133">CommonParameters</span></span>
<span data-ttu-id="67263-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="67263-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67263-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="67263-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67263-136">입력</span><span class="sxs-lookup"><span data-stu-id="67263-136">INPUTS</span></span>

### <span data-ttu-id="67263-137">System.String</span><span class="sxs-lookup"><span data-stu-id="67263-137">System.String</span></span>

## <span data-ttu-id="67263-138">출력</span><span class="sxs-lookup"><span data-stu-id="67263-138">OUTPUTS</span></span>

### <span data-ttu-id="67263-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="67263-139">System.Boolean</span></span>

## <span data-ttu-id="67263-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="67263-140">NOTES</span></span>

## <span data-ttu-id="67263-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67263-141">RELATED LINKS</span></span>

[<span data-ttu-id="67263-142">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="67263-142">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="67263-143">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="67263-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="67263-144">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="67263-144">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


