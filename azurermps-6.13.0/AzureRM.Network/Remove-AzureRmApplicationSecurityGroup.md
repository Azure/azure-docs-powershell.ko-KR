---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: a1d0935e7ca61d5eee3055ad9751fd794e093e8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526171"
---
# <span data-ttu-id="fb8d2-101">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fb8d2-101">Remove-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="fb8d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb8d2-102">SYNOPSIS</span></span>
<span data-ttu-id="fb8d2-103">응용 프로그램 보안 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb8d2-103">Removes an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb8d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fb8d2-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb8d2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fb8d2-105">DESCRIPTION</span></span>
<span data-ttu-id="fb8d2-106">**Remove-AzureRmApplicationSecurityGroup** cmdlet은 응용 프로그램 보안 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb8d2-106">The **Remove-AzureRmApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="fb8d2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fb8d2-107">EXAMPLES</span></span>

### <span data-ttu-id="fb8d2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fb8d2-108">Example 1</span></span>
```
PS C:\>Remove-AzureRmApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="fb8d2-109">이 명령은 Myapplicationsecurityname 이라는 리소스 그룹의 응용 프로그램 보안 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb8d2-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="fb8d2-110">변수</span><span class="sxs-lookup"><span data-stu-id="fb8d2-110">PARAMETERS</span></span>

### <span data-ttu-id="fb8d2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb8d2-111">-AsJob</span></span>
<span data-ttu-id="fb8d2-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fb8d2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb8d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb8d2-113">-DefaultProfile</span></span>
<span data-ttu-id="fb8d2-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb8d2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb8d2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fb8d2-115">-Force</span></span>
<span data-ttu-id="fb8d2-116">리소스를 삭제 하려는 경우 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="fb8d2-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="fb8d2-117">-이름</span><span class="sxs-lookup"><span data-stu-id="fb8d2-117">-Name</span></span>
<span data-ttu-id="fb8d2-118">응용 프로그램 보안 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb8d2-118">The name of the application security group.</span></span>

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

### <span data-ttu-id="fb8d2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb8d2-119">-PassThru</span></span>
<span data-ttu-id="fb8d2-120">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb8d2-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="fb8d2-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb8d2-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fb8d2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb8d2-122">-ResourceGroupName</span></span>
<span data-ttu-id="fb8d2-123">응용 프로그램 보안 그룹의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb8d2-123">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="fb8d2-124">-확인</span><span class="sxs-lookup"><span data-stu-id="fb8d2-124">-Confirm</span></span>
<span data-ttu-id="fb8d2-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb8d2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb8d2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb8d2-126">-WhatIf</span></span>
<span data-ttu-id="fb8d2-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fb8d2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb8d2-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb8d2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb8d2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb8d2-129">CommonParameters</span></span>
<span data-ttu-id="fb8d2-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb8d2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb8d2-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb8d2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb8d2-132">입력</span><span class="sxs-lookup"><span data-stu-id="fb8d2-132">INPUTS</span></span>

### <span data-ttu-id="fb8d2-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fb8d2-133">System.String</span></span>

## <span data-ttu-id="fb8d2-134">출력</span><span class="sxs-lookup"><span data-stu-id="fb8d2-134">OUTPUTS</span></span>

### <span data-ttu-id="fb8d2-135">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="fb8d2-135">System.Boolean</span></span>

## <span data-ttu-id="fb8d2-136">상속자</span><span class="sxs-lookup"><span data-stu-id="fb8d2-136">NOTES</span></span>

## <span data-ttu-id="fb8d2-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb8d2-137">RELATED LINKS</span></span>

[<span data-ttu-id="fb8d2-138">새로운 AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fb8d2-138">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="fb8d2-139">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fb8d2-139">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)
