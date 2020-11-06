---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: d1d07e27a7ad6fb6059cbfc8e4c972b1cedaf7e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536899"
---
# <span data-ttu-id="746d0-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="746d0-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="746d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="746d0-102">SYNOPSIS</span></span>
<span data-ttu-id="746d0-103">Azure App Service 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="746d0-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="746d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="746d0-104">SYNTAX</span></span>

### <span data-ttu-id="746d0-105">S1</span><span class="sxs-lookup"><span data-stu-id="746d0-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="746d0-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="746d0-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AppServicePlan] <ServerFarmWithRichSku>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="746d0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="746d0-107">DESCRIPTION</span></span>
<span data-ttu-id="746d0-108">**AzureRmAppServicePlan** Cmdlet은 Azure App Service 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="746d0-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="746d0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="746d0-109">EXAMPLES</span></span>

### <span data-ttu-id="746d0-110">예제 1: App Service 계획 제거</span><span class="sxs-lookup"><span data-stu-id="746d0-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="746d0-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoASP 이라는 Azure App Service 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="746d0-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="746d0-112">변수</span><span class="sxs-lookup"><span data-stu-id="746d0-112">PARAMETERS</span></span>

### <span data-ttu-id="746d0-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="746d0-113">-AppServicePlan</span></span>
<span data-ttu-id="746d0-114">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="746d0-114">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="746d0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="746d0-115">-Force</span></span>
<span data-ttu-id="746d0-116">강제로 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="746d0-116">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="746d0-117">-이름</span><span class="sxs-lookup"><span data-stu-id="746d0-117">-Name</span></span>
<span data-ttu-id="746d0-118">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="746d0-118">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="746d0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="746d0-119">-ResourceGroupName</span></span>
<span data-ttu-id="746d0-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="746d0-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="746d0-121">-확인</span><span class="sxs-lookup"><span data-stu-id="746d0-121">-Confirm</span></span>
<span data-ttu-id="746d0-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="746d0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="746d0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="746d0-123">-WhatIf</span></span>
<span data-ttu-id="746d0-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="746d0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="746d0-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="746d0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="746d0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="746d0-126">-DefaultProfile</span></span>
<span data-ttu-id="746d0-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="746d0-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="746d0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="746d0-128">CommonParameters</span></span>
<span data-ttu-id="746d0-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="746d0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="746d0-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="746d0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="746d0-131">입력</span><span class="sxs-lookup"><span data-stu-id="746d0-131">INPUTS</span></span>

### <span data-ttu-id="746d0-132">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="746d0-132">ServerFarmWithRichSku</span></span>
<span data-ttu-id="746d0-133">' AppServicePlan ' 매개 변수는 파이프라인에서 ' ServerFarmWithRichSku ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="746d0-133">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="746d0-134">출력</span><span class="sxs-lookup"><span data-stu-id="746d0-134">OUTPUTS</span></span>

### <span data-ttu-id="746d0-135">Microsoft Azure AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="746d0-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="746d0-136">상속자</span><span class="sxs-lookup"><span data-stu-id="746d0-136">NOTES</span></span>

## <span data-ttu-id="746d0-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="746d0-137">RELATED LINKS</span></span>

[<span data-ttu-id="746d0-138">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="746d0-138">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="746d0-139">새로운 AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="746d0-139">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="746d0-140">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="746d0-140">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


