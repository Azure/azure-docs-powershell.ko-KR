---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: 61cae1140ef0c46eee5857c15d0b6032a65caeb0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700147"
---
# <span data-ttu-id="5b9e9-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5b9e9-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="5b9e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b9e9-102">SYNOPSIS</span></span>
<span data-ttu-id="5b9e9-103">네트워크 인터페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-103">Removes a network interface.</span></span>

## <span data-ttu-id="5b9e9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5b9e9-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b9e9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5b9e9-105">DESCRIPTION</span></span>
<span data-ttu-id="5b9e9-106">**AzNetworkInterface** Cmdlet은 Azure 네트워크 인터페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="5b9e9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5b9e9-107">EXAMPLES</span></span>

### <span data-ttu-id="5b9e9-108">예제 1: 네트워크 인터페이스 제거</span><span class="sxs-lookup"><span data-stu-id="5b9e9-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="5b9e9-109">이 명령은 리소스 그룹 ResourceGroup1에서 네트워크 인터페이스 NetworkInterface1를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="5b9e9-110">*Force* 매개 변수는 사용 되지 않으므로 사용자에 게이 작업을 확인 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="5b9e9-111">예제 2: 네트워크 인터페이스 제거</span><span class="sxs-lookup"><span data-stu-id="5b9e9-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="5b9e9-112">이 명령은 리소스 그룹 ResourceGroup1의 모든 네트워크 인터페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="5b9e9-113">*Force* 매개 변수를 사용 하기 때문에 사용자에 게 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="5b9e9-114">변수</span><span class="sxs-lookup"><span data-stu-id="5b9e9-114">PARAMETERS</span></span>

### <span data-ttu-id="5b9e9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b9e9-115">-AsJob</span></span>
<span data-ttu-id="5b9e9-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5b9e9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b9e9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b9e9-117">-DefaultProfile</span></span>
<span data-ttu-id="5b9e9-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b9e9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5b9e9-119">-Force</span></span>
<span data-ttu-id="5b9e9-120">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5b9e9-121">-이름</span><span class="sxs-lookup"><span data-stu-id="5b9e9-121">-Name</span></span>
<span data-ttu-id="5b9e9-122">이 cmdlet이 제거 하는 네트워크 인터페이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5b9e9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b9e9-123">-PassThru</span></span>
<span data-ttu-id="5b9e9-124">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5b9e9-125">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5b9e9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b9e9-126">-ResourceGroupName</span></span>
<span data-ttu-id="5b9e9-127">이 cmdlet이 제거 하는 네트워크 인터페이스를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5b9e9-128">-확인</span><span class="sxs-lookup"><span data-stu-id="5b9e9-128">-Confirm</span></span>
<span data-ttu-id="5b9e9-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b9e9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b9e9-130">-WhatIf</span></span>
<span data-ttu-id="5b9e9-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b9e9-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b9e9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b9e9-133">CommonParameters</span></span>
<span data-ttu-id="5b9e9-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b9e9-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b9e9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b9e9-136">입력</span><span class="sxs-lookup"><span data-stu-id="5b9e9-136">INPUTS</span></span>

### <span data-ttu-id="5b9e9-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5b9e9-137">System.String</span></span>

## <span data-ttu-id="5b9e9-138">출력</span><span class="sxs-lookup"><span data-stu-id="5b9e9-138">OUTPUTS</span></span>

### <span data-ttu-id="5b9e9-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="5b9e9-139">System.Boolean</span></span>

## <span data-ttu-id="5b9e9-140">상속자</span><span class="sxs-lookup"><span data-stu-id="5b9e9-140">NOTES</span></span>

## <span data-ttu-id="5b9e9-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b9e9-141">RELATED LINKS</span></span>

[<span data-ttu-id="5b9e9-142">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5b9e9-142">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="5b9e9-143">새로운 AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5b9e9-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="5b9e9-144">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5b9e9-144">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


