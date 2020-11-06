---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: d5164e47dd759538fea6f0ab143ef9640055f1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528716"
---
# <span data-ttu-id="e9d05-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e9d05-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="e9d05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9d05-102">SYNOPSIS</span></span>
<span data-ttu-id="e9d05-103">Azure App Service 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d05-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9d05-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e9d05-104">SYNTAX</span></span>

### <span data-ttu-id="e9d05-105">S1</span><span class="sxs-lookup"><span data-stu-id="e9d05-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9d05-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="e9d05-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9d05-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e9d05-107">DESCRIPTION</span></span>
<span data-ttu-id="e9d05-108">**AzureRmAppServicePlan** Cmdlet은 Azure App Service 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d05-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="e9d05-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e9d05-109">EXAMPLES</span></span>

### <span data-ttu-id="e9d05-110">예제 1: App Service 계획 제거</span><span class="sxs-lookup"><span data-stu-id="e9d05-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="e9d05-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoASP 이라는 Azure App Service 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d05-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="e9d05-112">변수</span><span class="sxs-lookup"><span data-stu-id="e9d05-112">PARAMETERS</span></span>

### <span data-ttu-id="e9d05-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e9d05-113">-AppServicePlan</span></span>
<span data-ttu-id="e9d05-114">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="e9d05-114">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9d05-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9d05-115">-DefaultProfile</span></span>
<span data-ttu-id="e9d05-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e9d05-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9d05-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e9d05-117">-Force</span></span>
<span data-ttu-id="e9d05-118">강제로 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="e9d05-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="e9d05-119">-이름</span><span class="sxs-lookup"><span data-stu-id="e9d05-119">-Name</span></span>
<span data-ttu-id="e9d05-120">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="e9d05-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="e9d05-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9d05-121">-ResourceGroupName</span></span>
<span data-ttu-id="e9d05-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e9d05-122">Resource Group Name</span></span>

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

### <span data-ttu-id="e9d05-123">-확인</span><span class="sxs-lookup"><span data-stu-id="e9d05-123">-Confirm</span></span>
<span data-ttu-id="e9d05-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d05-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9d05-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9d05-125">-WhatIf</span></span>
<span data-ttu-id="e9d05-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e9d05-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9d05-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9d05-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9d05-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9d05-128">-AsJob</span></span>
<span data-ttu-id="e9d05-129">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e9d05-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e9d05-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9d05-130">CommonParameters</span></span>
<span data-ttu-id="e9d05-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d05-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9d05-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9d05-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9d05-133">입력</span><span class="sxs-lookup"><span data-stu-id="e9d05-133">INPUTS</span></span>

### <span data-ttu-id="e9d05-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="e9d05-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="e9d05-135">' AppServicePlan ' 매개 변수는 파이프라인에서 ' ServerFarmWithRichSku ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9d05-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="e9d05-136">출력</span><span class="sxs-lookup"><span data-stu-id="e9d05-136">OUTPUTS</span></span>

### <span data-ttu-id="e9d05-137">Microsoft Azure AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e9d05-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="e9d05-138">상속자</span><span class="sxs-lookup"><span data-stu-id="e9d05-138">NOTES</span></span>

## <span data-ttu-id="e9d05-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9d05-139">RELATED LINKS</span></span>

[<span data-ttu-id="e9d05-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e9d05-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="e9d05-141">새로운 AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e9d05-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="e9d05-142">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e9d05-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


