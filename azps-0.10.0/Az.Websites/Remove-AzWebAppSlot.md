---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 04813b04d3d2499de549655edb6398550ce25536
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876120"
---
# <span data-ttu-id="36dad-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="36dad-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="36dad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36dad-102">SYNOPSIS</span></span>

## <span data-ttu-id="36dad-103">구문과</span><span class="sxs-lookup"><span data-stu-id="36dad-103">SYNTAX</span></span>

### <span data-ttu-id="36dad-104">S1</span><span class="sxs-lookup"><span data-stu-id="36dad-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36dad-105">구성원과</span><span class="sxs-lookup"><span data-stu-id="36dad-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-WebApp] <Site> [-AsJob][-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36dad-106">설명은</span><span class="sxs-lookup"><span data-stu-id="36dad-106">DESCRIPTION</span></span>
<span data-ttu-id="36dad-107">**AzWebAppSlot** cmdlet은 리소스 그룹과 웹 앱 이름을 제공 하는 Azure Web app 슬롯을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="36dad-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="36dad-108">이 cmdlet은 기본적으로 모든 슬롯과 메트릭스도 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="36dad-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="36dad-109">예제의</span><span class="sxs-lookup"><span data-stu-id="36dad-109">EXAMPLES</span></span>

### <span data-ttu-id="36dad-110">예제 1: 웹 앱 슬롯 제거</span><span class="sxs-lookup"><span data-stu-id="36dad-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "ContosoSlot"
```

<span data-ttu-id="36dad-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 웹 앱 ContosoSite와 연결 된 Slot001 이라는 슬롯을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="36dad-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="36dad-112">변수</span><span class="sxs-lookup"><span data-stu-id="36dad-112">PARAMETERS</span></span>

### <span data-ttu-id="36dad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36dad-113">-DefaultProfile</span></span>
<span data-ttu-id="36dad-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36dad-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36dad-115">-Force</span><span class="sxs-lookup"><span data-stu-id="36dad-115">-Force</span></span>
<span data-ttu-id="36dad-116">강제로 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="36dad-116">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="36dad-117">-이름</span><span class="sxs-lookup"><span data-stu-id="36dad-117">-Name</span></span>
<span data-ttu-id="36dad-118">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="36dad-118">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36dad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36dad-119">-ResourceGroupName</span></span>
<span data-ttu-id="36dad-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="36dad-120">Resource Group Name</span></span>

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

### <span data-ttu-id="36dad-121">-슬롯</span><span class="sxs-lookup"><span data-stu-id="36dad-121">-Slot</span></span>
<span data-ttu-id="36dad-122">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="36dad-122">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36dad-123">-Web app</span><span class="sxs-lookup"><span data-stu-id="36dad-123">-WebApp</span></span>
<span data-ttu-id="36dad-124">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="36dad-124">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36dad-125">-확인</span><span class="sxs-lookup"><span data-stu-id="36dad-125">-Confirm</span></span>
<span data-ttu-id="36dad-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="36dad-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36dad-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36dad-127">-WhatIf</span></span>
<span data-ttu-id="36dad-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="36dad-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36dad-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36dad-129">The cmdlet is not run.</span></span>

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
### <span data-ttu-id="36dad-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36dad-130">-AsJob</span></span>
<span data-ttu-id="36dad-131">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="36dad-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36dad-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36dad-132">CommonParameters</span></span>
<span data-ttu-id="36dad-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="36dad-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36dad-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36dad-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36dad-135">입력</span><span class="sxs-lookup"><span data-stu-id="36dad-135">INPUTS</span></span>

### <span data-ttu-id="36dad-136">Site</span><span class="sxs-lookup"><span data-stu-id="36dad-136">Site</span></span>
<span data-ttu-id="36dad-137">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="36dad-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="36dad-138">출력</span><span class="sxs-lookup"><span data-stu-id="36dad-138">OUTPUTS</span></span>

### <span data-ttu-id="36dad-139">Microsoft Azure AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="36dad-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="36dad-140">상속자</span><span class="sxs-lookup"><span data-stu-id="36dad-140">NOTES</span></span>

## <span data-ttu-id="36dad-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36dad-141">RELATED LINKS</span></span>

[<span data-ttu-id="36dad-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="36dad-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="36dad-143">새로운 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="36dad-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="36dad-144">다시 시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="36dad-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="36dad-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="36dad-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="36dad-146">시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="36dad-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="36dad-147">중지-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="36dad-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="36dad-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="36dad-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
