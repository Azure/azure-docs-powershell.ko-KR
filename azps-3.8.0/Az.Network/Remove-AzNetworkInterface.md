---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: f4de49bb2e35bf3d392fba06d663800a5bdc44a6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044021"
---
# <span data-ttu-id="1ae14-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1ae14-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="1ae14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ae14-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae14-103">네트워크 인터페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ae14-103">Removes a network interface.</span></span>

## <span data-ttu-id="1ae14-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1ae14-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ae14-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1ae14-105">DESCRIPTION</span></span>
<span data-ttu-id="1ae14-106">**AzNetworkInterface** Cmdlet은 Azure 네트워크 인터페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ae14-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="1ae14-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1ae14-107">EXAMPLES</span></span>

### <span data-ttu-id="1ae14-108">예제 1: 네트워크 인터페이스 제거</span><span class="sxs-lookup"><span data-stu-id="1ae14-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="1ae14-109">이 명령은 리소스 그룹 ResourceGroup1에서 네트워크 인터페이스 NetworkInterface1를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ae14-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="1ae14-110">*Force* 매개 변수는 사용 되지 않으므로 사용자에 게이 작업을 확인 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ae14-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="1ae14-111">예제 2: 네트워크 인터페이스 제거</span><span class="sxs-lookup"><span data-stu-id="1ae14-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="1ae14-112">이 명령은 리소스 그룹 ResourceGroup1의 모든 네트워크 인터페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ae14-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="1ae14-113">*Force* 매개 변수를 사용 하기 때문에 사용자에 게 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ae14-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="1ae14-114">변수</span><span class="sxs-lookup"><span data-stu-id="1ae14-114">PARAMETERS</span></span>

### <span data-ttu-id="1ae14-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ae14-115">-AsJob</span></span>
<span data-ttu-id="1ae14-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1ae14-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ae14-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae14-117">-DefaultProfile</span></span>
<span data-ttu-id="1ae14-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ae14-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ae14-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1ae14-119">-Force</span></span>
<span data-ttu-id="1ae14-120">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ae14-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1ae14-121">-이름</span><span class="sxs-lookup"><span data-stu-id="1ae14-121">-Name</span></span>
<span data-ttu-id="1ae14-122">이 cmdlet이 제거 하는 네트워크 인터페이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ae14-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1ae14-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ae14-123">-PassThru</span></span>
<span data-ttu-id="1ae14-124">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ae14-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1ae14-125">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ae14-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1ae14-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae14-126">-ResourceGroupName</span></span>
<span data-ttu-id="1ae14-127">이 cmdlet이 제거 하는 네트워크 인터페이스를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ae14-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1ae14-128">-확인</span><span class="sxs-lookup"><span data-stu-id="1ae14-128">-Confirm</span></span>
<span data-ttu-id="1ae14-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ae14-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ae14-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ae14-130">-WhatIf</span></span>
<span data-ttu-id="1ae14-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1ae14-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ae14-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ae14-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ae14-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae14-133">CommonParameters</span></span>
<span data-ttu-id="1ae14-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ae14-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae14-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ae14-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae14-136">입력</span><span class="sxs-lookup"><span data-stu-id="1ae14-136">INPUTS</span></span>

### <span data-ttu-id="1ae14-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1ae14-137">System.String</span></span>

## <span data-ttu-id="1ae14-138">출력</span><span class="sxs-lookup"><span data-stu-id="1ae14-138">OUTPUTS</span></span>

### <span data-ttu-id="1ae14-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1ae14-139">System.Boolean</span></span>

## <span data-ttu-id="1ae14-140">상속자</span><span class="sxs-lookup"><span data-stu-id="1ae14-140">NOTES</span></span>

## <span data-ttu-id="1ae14-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ae14-141">RELATED LINKS</span></span>

[<span data-ttu-id="1ae14-142">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1ae14-142">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="1ae14-143">새로운 AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1ae14-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="1ae14-144">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1ae14-144">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


