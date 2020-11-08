---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
ms.openlocfilehash: c5a5cbbbc46106fe6c388ee8f16117411f03fe0c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217252"
---
# <span data-ttu-id="03485-101">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="03485-101">Remove-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="03485-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03485-102">SYNOPSIS</span></span>
<span data-ttu-id="03485-103">네트워크 보안 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="03485-103">Removes a network security group.</span></span>

## <span data-ttu-id="03485-104">구문과</span><span class="sxs-lookup"><span data-stu-id="03485-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03485-105">설명은</span><span class="sxs-lookup"><span data-stu-id="03485-105">DESCRIPTION</span></span>
<span data-ttu-id="03485-106">**AzNetworkSecurityGroup** Cmdlet은 Azure 네트워크 보안 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="03485-106">The **Remove-AzNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="03485-107">예제의</span><span class="sxs-lookup"><span data-stu-id="03485-107">EXAMPLES</span></span>

### <span data-ttu-id="03485-108">예제 1: 네트워크 보안 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="03485-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="03485-109">이 명령은 TestRG 이라는 리소스 그룹에 있는 NSG-FrontEnd 라는 보안 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="03485-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="03485-110">변수</span><span class="sxs-lookup"><span data-stu-id="03485-110">PARAMETERS</span></span>

### <span data-ttu-id="03485-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03485-111">-AsJob</span></span>
<span data-ttu-id="03485-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="03485-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03485-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03485-113">-DefaultProfile</span></span>
<span data-ttu-id="03485-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03485-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03485-115">-Force</span><span class="sxs-lookup"><span data-stu-id="03485-115">-Force</span></span>
<span data-ttu-id="03485-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="03485-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="03485-117">-이름</span><span class="sxs-lookup"><span data-stu-id="03485-117">-Name</span></span>
<span data-ttu-id="03485-118">이 cmdlet이 제거 하는 네트워크 보안 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03485-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="03485-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03485-119">-PassThru</span></span>
<span data-ttu-id="03485-120">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="03485-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="03485-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03485-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="03485-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03485-122">-ResourceGroupName</span></span>
<span data-ttu-id="03485-123">이 cmdlet이 네트워크 보안 그룹을 제거 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03485-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="03485-124">-확인</span><span class="sxs-lookup"><span data-stu-id="03485-124">-Confirm</span></span>
<span data-ttu-id="03485-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="03485-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03485-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03485-126">-WhatIf</span></span>
<span data-ttu-id="03485-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="03485-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03485-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03485-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03485-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03485-129">CommonParameters</span></span>
<span data-ttu-id="03485-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="03485-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03485-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03485-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03485-132">입력</span><span class="sxs-lookup"><span data-stu-id="03485-132">INPUTS</span></span>

### <span data-ttu-id="03485-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="03485-133">System.String</span></span>

## <span data-ttu-id="03485-134">출력</span><span class="sxs-lookup"><span data-stu-id="03485-134">OUTPUTS</span></span>

### <span data-ttu-id="03485-135">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="03485-135">System.Boolean</span></span>

## <span data-ttu-id="03485-136">상속자</span><span class="sxs-lookup"><span data-stu-id="03485-136">NOTES</span></span>

## <span data-ttu-id="03485-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03485-137">RELATED LINKS</span></span>

[<span data-ttu-id="03485-138">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="03485-138">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="03485-139">새로운 AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="03485-139">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="03485-140">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="03485-140">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


