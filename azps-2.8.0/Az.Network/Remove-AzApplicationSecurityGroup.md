---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 0af35c08cce181ba96f15ca77c0f17f96cfeb32e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869753"
---
# <span data-ttu-id="139c0-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="139c0-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="139c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="139c0-102">SYNOPSIS</span></span>
<span data-ttu-id="139c0-103">응용 프로그램 보안 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="139c0-103">Removes an application security group.</span></span>

## <span data-ttu-id="139c0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="139c0-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="139c0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="139c0-105">DESCRIPTION</span></span>
<span data-ttu-id="139c0-106">**Remove-AzApplicationSecurityGroup** cmdlet은 응용 프로그램 보안 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="139c0-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="139c0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="139c0-107">EXAMPLES</span></span>

### <span data-ttu-id="139c0-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="139c0-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="139c0-109">이 명령은 Myapplicationsecurityname 이라는 리소스 그룹의 응용 프로그램 보안 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="139c0-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="139c0-110">변수</span><span class="sxs-lookup"><span data-stu-id="139c0-110">PARAMETERS</span></span>

### <span data-ttu-id="139c0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="139c0-111">-AsJob</span></span>
<span data-ttu-id="139c0-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="139c0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="139c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="139c0-113">-DefaultProfile</span></span>
<span data-ttu-id="139c0-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="139c0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="139c0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="139c0-115">-Force</span></span>
<span data-ttu-id="139c0-116">리소스를 삭제 하려는 경우 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="139c0-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="139c0-117">-이름</span><span class="sxs-lookup"><span data-stu-id="139c0-117">-Name</span></span>
<span data-ttu-id="139c0-118">응용 프로그램 보안 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="139c0-118">The name of the application security group.</span></span>

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

### <span data-ttu-id="139c0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="139c0-119">-PassThru</span></span>
<span data-ttu-id="139c0-120">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="139c0-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="139c0-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="139c0-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="139c0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="139c0-122">-ResourceGroupName</span></span>
<span data-ttu-id="139c0-123">응용 프로그램 보안 그룹의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="139c0-123">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="139c0-124">-확인</span><span class="sxs-lookup"><span data-stu-id="139c0-124">-Confirm</span></span>
<span data-ttu-id="139c0-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="139c0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="139c0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="139c0-126">-WhatIf</span></span>
<span data-ttu-id="139c0-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="139c0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="139c0-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="139c0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="139c0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="139c0-129">CommonParameters</span></span>
<span data-ttu-id="139c0-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="139c0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="139c0-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="139c0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="139c0-132">입력</span><span class="sxs-lookup"><span data-stu-id="139c0-132">INPUTS</span></span>

### <span data-ttu-id="139c0-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="139c0-133">System.String</span></span>

## <span data-ttu-id="139c0-134">출력</span><span class="sxs-lookup"><span data-stu-id="139c0-134">OUTPUTS</span></span>

### <span data-ttu-id="139c0-135">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="139c0-135">System.Boolean</span></span>

## <span data-ttu-id="139c0-136">상속자</span><span class="sxs-lookup"><span data-stu-id="139c0-136">NOTES</span></span>

## <span data-ttu-id="139c0-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="139c0-137">RELATED LINKS</span></span>

[<span data-ttu-id="139c0-138">새로운 AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="139c0-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="139c0-139">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="139c0-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
