---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationsecuritygroup
schema: 2.0.0
ms.openlocfilehash: 48121e165eea27b57ec36301a657a6778f4c14b7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880965"
---
# <span data-ttu-id="0d938-101">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0d938-101">Remove-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="0d938-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d938-102">SYNOPSIS</span></span>
<span data-ttu-id="0d938-103">응용 프로그램 보안 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d938-103">Removes an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d938-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0d938-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d938-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0d938-105">DESCRIPTION</span></span>
<span data-ttu-id="0d938-106">**Remove-AzureRmApplicationSecurityGroup** cmdlet은 응용 프로그램 보안 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d938-106">The **Remove-AzureRmApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="0d938-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0d938-107">EXAMPLES</span></span>

### <span data-ttu-id="0d938-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0d938-108">Example 1</span></span>
```
PS C:\>Remove-AzureRmApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="0d938-109">이 명령은 Myapplicationsecurityname 이라는 리소스 그룹의 응용 프로그램 보안 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d938-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="0d938-110">변수</span><span class="sxs-lookup"><span data-stu-id="0d938-110">PARAMETERS</span></span>

### <span data-ttu-id="0d938-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d938-111">-DefaultProfile</span></span>
<span data-ttu-id="0d938-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d938-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d938-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0d938-113">-Force</span></span>
<span data-ttu-id="0d938-114">리소스를 삭제 하려는 경우 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="0d938-114">Do not ask for confirmation if you want to delete resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d938-115">-이름</span><span class="sxs-lookup"><span data-stu-id="0d938-115">-Name</span></span>
<span data-ttu-id="0d938-116">응용 프로그램 보안 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d938-116">The name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d938-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d938-117">-PassThru</span></span>
<span data-ttu-id="0d938-118">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d938-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="0d938-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d938-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d938-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d938-120">-ResourceGroupName</span></span>
<span data-ttu-id="0d938-121">응용 프로그램 보안 그룹의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d938-121">The resource group name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d938-122">-확인</span><span class="sxs-lookup"><span data-stu-id="0d938-122">-Confirm</span></span>
<span data-ttu-id="0d938-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d938-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d938-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d938-124">-WhatIf</span></span>
<span data-ttu-id="0d938-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0d938-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d938-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d938-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d938-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d938-127">CommonParameters</span></span>
<span data-ttu-id="0d938-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d938-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d938-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d938-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d938-130">입력</span><span class="sxs-lookup"><span data-stu-id="0d938-130">INPUTS</span></span>

### <span data-ttu-id="0d938-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0d938-131">System.String</span></span>

## <span data-ttu-id="0d938-132">출력</span><span class="sxs-lookup"><span data-stu-id="0d938-132">OUTPUTS</span></span>

### <span data-ttu-id="0d938-133">System. 개체</span><span class="sxs-lookup"><span data-stu-id="0d938-133">System.Object</span></span>

## <span data-ttu-id="0d938-134">상속자</span><span class="sxs-lookup"><span data-stu-id="0d938-134">NOTES</span></span>

## <span data-ttu-id="0d938-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d938-135">RELATED LINKS</span></span>

[<span data-ttu-id="0d938-136">새로운 AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0d938-136">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="0d938-137">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0d938-137">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)
