---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: 3d0e3ad30df71700eb83938181ed86a97a77528a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876124"
---
# <span data-ttu-id="cc947-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cc947-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="cc947-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc947-102">SYNOPSIS</span></span>
<span data-ttu-id="cc947-103">Azure App Service 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc947-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="cc947-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cc947-104">SYNTAX</span></span>

### <span data-ttu-id="cc947-105">S1</span><span class="sxs-lookup"><span data-stu-id="cc947-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc947-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="cc947-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AppServicePlan] <AppServicePlan> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc947-107">설명은</span><span class="sxs-lookup"><span data-stu-id="cc947-107">DESCRIPTION</span></span>
<span data-ttu-id="cc947-108">**AzAppServicePlan** Cmdlet은 Azure App Service 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc947-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="cc947-109">예제의</span><span class="sxs-lookup"><span data-stu-id="cc947-109">EXAMPLES</span></span>

### <span data-ttu-id="cc947-110">예제 1: App Service 계획 제거</span><span class="sxs-lookup"><span data-stu-id="cc947-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="cc947-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoASP 이라는 Azure App Service 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc947-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="cc947-112">변수</span><span class="sxs-lookup"><span data-stu-id="cc947-112">PARAMETERS</span></span>

### <span data-ttu-id="cc947-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cc947-113">-AppServicePlan</span></span>
<span data-ttu-id="cc947-114">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="cc947-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="cc947-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc947-115">-DefaultProfile</span></span>
<span data-ttu-id="cc947-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cc947-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc947-117">-Force</span><span class="sxs-lookup"><span data-stu-id="cc947-117">-Force</span></span>
<span data-ttu-id="cc947-118">강제로 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="cc947-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="cc947-119">-이름</span><span class="sxs-lookup"><span data-stu-id="cc947-119">-Name</span></span>
<span data-ttu-id="cc947-120">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="cc947-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="cc947-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc947-121">-ResourceGroupName</span></span>
<span data-ttu-id="cc947-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="cc947-122">Resource Group Name</span></span>

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

### <span data-ttu-id="cc947-123">-확인</span><span class="sxs-lookup"><span data-stu-id="cc947-123">-Confirm</span></span>
<span data-ttu-id="cc947-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc947-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc947-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc947-125">-WhatIf</span></span>
<span data-ttu-id="cc947-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cc947-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc947-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cc947-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc947-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc947-128">-AsJob</span></span>
<span data-ttu-id="cc947-129">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cc947-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc947-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc947-130">CommonParameters</span></span>
<span data-ttu-id="cc947-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc947-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc947-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc947-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc947-133">입력</span><span class="sxs-lookup"><span data-stu-id="cc947-133">INPUTS</span></span>

### <span data-ttu-id="cc947-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="cc947-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="cc947-135">' AppServicePlan ' 매개 변수는 파이프라인에서 ' ServerFarmWithRichSku ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc947-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="cc947-136">출력</span><span class="sxs-lookup"><span data-stu-id="cc947-136">OUTPUTS</span></span>

### <span data-ttu-id="cc947-137">Microsoft Azure AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="cc947-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="cc947-138">상속자</span><span class="sxs-lookup"><span data-stu-id="cc947-138">NOTES</span></span>

## <span data-ttu-id="cc947-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cc947-139">RELATED LINKS</span></span>

[<span data-ttu-id="cc947-140">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cc947-140">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="cc947-141">새로운 AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cc947-141">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="cc947-142">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cc947-142">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


