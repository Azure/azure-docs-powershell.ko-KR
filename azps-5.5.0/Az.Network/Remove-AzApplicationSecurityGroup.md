---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 562a2fbf02bd6389b28543f09ace1c59b2e9ed1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202596"
---
# <span data-ttu-id="b367f-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b367f-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="b367f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b367f-102">SYNOPSIS</span></span>
<span data-ttu-id="b367f-103">애플리케이션 보안 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b367f-103">Removes an application security group.</span></span>

## <span data-ttu-id="b367f-104">구문</span><span class="sxs-lookup"><span data-stu-id="b367f-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b367f-105">설명</span><span class="sxs-lookup"><span data-stu-id="b367f-105">DESCRIPTION</span></span>
<span data-ttu-id="b367f-106">**Remove-AzApplicationSecurityGroup** cmdlet은 애플리케이션 보안 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b367f-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="b367f-107">예제</span><span class="sxs-lookup"><span data-stu-id="b367f-107">EXAMPLES</span></span>

### <span data-ttu-id="b367f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b367f-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="b367f-109">이 명령은 MyResourceGroup이라는 리소스 그룹에서 MyApplicationSecurityGrouo라는 애플리케이션 보안 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b367f-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="b367f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b367f-110">PARAMETERS</span></span>

### <span data-ttu-id="b367f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b367f-111">-AsJob</span></span>
<span data-ttu-id="b367f-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b367f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b367f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b367f-113">-DefaultProfile</span></span>
<span data-ttu-id="b367f-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b367f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b367f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b367f-115">-Force</span></span>
<span data-ttu-id="b367f-116">리소스를 삭제하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b367f-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="b367f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b367f-117">-Name</span></span>
<span data-ttu-id="b367f-118">애플리케이션 보안 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b367f-118">The name of the application security group.</span></span>

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

### <span data-ttu-id="b367f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b367f-119">-PassThru</span></span>
<span data-ttu-id="b367f-120">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b367f-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="b367f-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b367f-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b367f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b367f-122">-ResourceGroupName</span></span>
<span data-ttu-id="b367f-123">애플리케이션 보안 그룹의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b367f-123">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="b367f-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b367f-124">-Confirm</span></span>
<span data-ttu-id="b367f-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b367f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b367f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b367f-126">-WhatIf</span></span>
<span data-ttu-id="b367f-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b367f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b367f-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b367f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b367f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b367f-129">CommonParameters</span></span>
<span data-ttu-id="b367f-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b367f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b367f-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b367f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b367f-132">입력</span><span class="sxs-lookup"><span data-stu-id="b367f-132">INPUTS</span></span>

### <span data-ttu-id="b367f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b367f-133">System.String</span></span>

## <span data-ttu-id="b367f-134">출력</span><span class="sxs-lookup"><span data-stu-id="b367f-134">OUTPUTS</span></span>

### <span data-ttu-id="b367f-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b367f-135">System.Boolean</span></span>

## <span data-ttu-id="b367f-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b367f-136">NOTES</span></span>

## <span data-ttu-id="b367f-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b367f-137">RELATED LINKS</span></span>

[<span data-ttu-id="b367f-138">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b367f-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="b367f-139">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b367f-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
