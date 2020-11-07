---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 27d1e45a9e2c85fb3d2f7470db97ce2426f62a19
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882322"
---
# <span data-ttu-id="fe0ea-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="fe0ea-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="fe0ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe0ea-102">SYNOPSIS</span></span>
<span data-ttu-id="fe0ea-103">컨테이너 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe0ea-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe0ea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fe0ea-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe0ea-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fe0ea-105">DESCRIPTION</span></span>
<span data-ttu-id="fe0ea-106">**AzureRmContainerService** Cmdlet은 Azure 계정에서 컨테이너 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe0ea-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="fe0ea-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fe0ea-107">EXAMPLES</span></span>

### <span data-ttu-id="fe0ea-108">예제 1: 컨테이너 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="fe0ea-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="fe0ea-109">이 명령은 CSResourceGroup17 이라는 컨테이너 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe0ea-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="fe0ea-110">변수</span><span class="sxs-lookup"><span data-stu-id="fe0ea-110">PARAMETERS</span></span>

### <span data-ttu-id="fe0ea-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe0ea-111">-AsJob</span></span>
<span data-ttu-id="fe0ea-112">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe0ea-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fe0ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe0ea-113">-DefaultProfile</span></span>
<span data-ttu-id="fe0ea-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fe0ea-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe0ea-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fe0ea-115">-Force</span></span>
<span data-ttu-id="fe0ea-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe0ea-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fe0ea-117">-이름</span><span class="sxs-lookup"><span data-stu-id="fe0ea-117">-Name</span></span>
<span data-ttu-id="fe0ea-118">이 cmdlet이 제거 하는 컨테이너 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe0ea-118">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe0ea-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe0ea-119">-ResourceGroupName</span></span>
<span data-ttu-id="fe0ea-120">이 cmdlet이 제거 하는 컨테이너 서비스의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe0ea-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe0ea-121">-확인</span><span class="sxs-lookup"><span data-stu-id="fe0ea-121">-Confirm</span></span>
<span data-ttu-id="fe0ea-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe0ea-122">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe0ea-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe0ea-123">-WhatIf</span></span>
<span data-ttu-id="fe0ea-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fe0ea-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe0ea-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fe0ea-125">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe0ea-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe0ea-126">CommonParameters</span></span>
<span data-ttu-id="fe0ea-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe0ea-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe0ea-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe0ea-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe0ea-129">입력</span><span class="sxs-lookup"><span data-stu-id="fe0ea-129">INPUTS</span></span>

### <span data-ttu-id="fe0ea-130">않아야</span><span class="sxs-lookup"><span data-stu-id="fe0ea-130">None</span></span>
<span data-ttu-id="fe0ea-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fe0ea-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fe0ea-132">출력</span><span class="sxs-lookup"><span data-stu-id="fe0ea-132">OUTPUTS</span></span>

### <span data-ttu-id="fe0ea-133">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="fe0ea-133">System.Void</span></span>

## <span data-ttu-id="fe0ea-134">상속자</span><span class="sxs-lookup"><span data-stu-id="fe0ea-134">NOTES</span></span>

## <span data-ttu-id="fe0ea-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe0ea-135">RELATED LINKS</span></span>

[<span data-ttu-id="fe0ea-136">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="fe0ea-136">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="fe0ea-137">새로운 AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="fe0ea-137">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="fe0ea-138">업데이트-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="fe0ea-138">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


