---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: e8ce0397a59a72e2960a8e0af978c1b5484c53af
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880294"
---
# <span data-ttu-id="2dfb4-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2dfb4-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="2dfb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dfb4-102">SYNOPSIS</span></span>
<span data-ttu-id="2dfb4-103">Azure App Service 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dfb4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2dfb4-104">SYNTAX</span></span>

### <span data-ttu-id="2dfb4-105">S1</span><span class="sxs-lookup"><span data-stu-id="2dfb4-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dfb4-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="2dfb4-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AppServicePlan] <AppServicePlan> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dfb4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2dfb4-107">DESCRIPTION</span></span>
<span data-ttu-id="2dfb4-108">**AzureRmAppServicePlan** Cmdlet은 Azure App Service 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="2dfb4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2dfb4-109">EXAMPLES</span></span>

### <span data-ttu-id="2dfb4-110">예제 1: App Service 계획 제거</span><span class="sxs-lookup"><span data-stu-id="2dfb4-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="2dfb4-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoASP 이라는 Azure App Service 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="2dfb4-112">변수</span><span class="sxs-lookup"><span data-stu-id="2dfb4-112">PARAMETERS</span></span>

### <span data-ttu-id="2dfb4-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2dfb4-113">-AppServicePlan</span></span>
<span data-ttu-id="2dfb4-114">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="2dfb4-114">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2dfb4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dfb4-115">-DefaultProfile</span></span>
<span data-ttu-id="2dfb4-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dfb4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2dfb4-117">-Force</span></span>
<span data-ttu-id="2dfb4-118">강제로 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="2dfb4-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="2dfb4-119">-이름</span><span class="sxs-lookup"><span data-stu-id="2dfb4-119">-Name</span></span>
<span data-ttu-id="2dfb4-120">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="2dfb4-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dfb4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dfb4-121">-ResourceGroupName</span></span>
<span data-ttu-id="2dfb4-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2dfb4-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dfb4-123">-확인</span><span class="sxs-lookup"><span data-stu-id="2dfb4-123">-Confirm</span></span>
<span data-ttu-id="2dfb4-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dfb4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dfb4-125">-WhatIf</span></span>
<span data-ttu-id="2dfb4-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dfb4-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dfb4-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2dfb4-128">-AsJob</span></span>
<span data-ttu-id="2dfb4-129">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2dfb4-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2dfb4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dfb4-130">CommonParameters</span></span>
<span data-ttu-id="2dfb4-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dfb4-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dfb4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dfb4-133">입력</span><span class="sxs-lookup"><span data-stu-id="2dfb4-133">INPUTS</span></span>

### <span data-ttu-id="2dfb4-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="2dfb4-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="2dfb4-135">' AppServicePlan ' 매개 변수는 파이프라인에서 ' ServerFarmWithRichSku ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="2dfb4-136">출력</span><span class="sxs-lookup"><span data-stu-id="2dfb4-136">OUTPUTS</span></span>

### <span data-ttu-id="2dfb4-137">Microsoft Azure AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2dfb4-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="2dfb4-138">상속자</span><span class="sxs-lookup"><span data-stu-id="2dfb4-138">NOTES</span></span>

## <span data-ttu-id="2dfb4-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2dfb4-139">RELATED LINKS</span></span>

[<span data-ttu-id="2dfb4-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2dfb4-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="2dfb4-141">새로운 AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2dfb4-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="2dfb4-142">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2dfb4-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


