---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: eeaeb43083a2b125147df5d91516b71bdff377a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534544"
---
# <span data-ttu-id="d37c8-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d37c8-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="d37c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d37c8-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d37c8-103">구문과</span><span class="sxs-lookup"><span data-stu-id="d37c8-103">SYNTAX</span></span>

### <span data-ttu-id="d37c8-104">S1</span><span class="sxs-lookup"><span data-stu-id="d37c8-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d37c8-105">구성원과</span><span class="sxs-lookup"><span data-stu-id="d37c8-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-WebApp] <Site> [-AsJob][-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d37c8-106">설명은</span><span class="sxs-lookup"><span data-stu-id="d37c8-106">DESCRIPTION</span></span>
<span data-ttu-id="d37c8-107">**AzureRmWebAppSlot** cmdlet은 리소스 그룹과 웹 앱 이름을 제공 하는 Azure Web app 슬롯을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d37c8-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="d37c8-108">이 cmdlet은 기본적으로 모든 슬롯과 메트릭스도 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d37c8-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="d37c8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d37c8-109">EXAMPLES</span></span>

### <span data-ttu-id="d37c8-110">예제 1: 웹 앱 슬롯 제거</span><span class="sxs-lookup"><span data-stu-id="d37c8-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "ContosoSlot"
```

<span data-ttu-id="d37c8-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 웹 앱 ContosoSite와 연결 된 Slot001 이라는 슬롯을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d37c8-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d37c8-112">변수</span><span class="sxs-lookup"><span data-stu-id="d37c8-112">PARAMETERS</span></span>

### <span data-ttu-id="d37c8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37c8-113">-DefaultProfile</span></span>
<span data-ttu-id="d37c8-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d37c8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d37c8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d37c8-115">-Force</span></span>
<span data-ttu-id="d37c8-116">강제로 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="d37c8-116">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="d37c8-117">-이름</span><span class="sxs-lookup"><span data-stu-id="d37c8-117">-Name</span></span>
<span data-ttu-id="d37c8-118">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="d37c8-118">WebApp Name</span></span>

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

### <span data-ttu-id="d37c8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d37c8-119">-ResourceGroupName</span></span>
<span data-ttu-id="d37c8-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d37c8-120">Resource Group Name</span></span>

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

### <span data-ttu-id="d37c8-121">-슬롯</span><span class="sxs-lookup"><span data-stu-id="d37c8-121">-Slot</span></span>
<span data-ttu-id="d37c8-122">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="d37c8-122">WebApp Slot Name</span></span>

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

### <span data-ttu-id="d37c8-123">-Web app</span><span class="sxs-lookup"><span data-stu-id="d37c8-123">-WebApp</span></span>
<span data-ttu-id="d37c8-124">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="d37c8-124">WebApp Object</span></span>

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

### <span data-ttu-id="d37c8-125">-확인</span><span class="sxs-lookup"><span data-stu-id="d37c8-125">-Confirm</span></span>
<span data-ttu-id="d37c8-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d37c8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d37c8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d37c8-127">-WhatIf</span></span>
<span data-ttu-id="d37c8-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d37c8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d37c8-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d37c8-129">The cmdlet is not run.</span></span>

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
### <span data-ttu-id="d37c8-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d37c8-130">-AsJob</span></span>
<span data-ttu-id="d37c8-131">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d37c8-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d37c8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37c8-132">CommonParameters</span></span>
<span data-ttu-id="d37c8-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d37c8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37c8-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d37c8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37c8-135">입력</span><span class="sxs-lookup"><span data-stu-id="d37c8-135">INPUTS</span></span>

### <span data-ttu-id="d37c8-136">Site</span><span class="sxs-lookup"><span data-stu-id="d37c8-136">Site</span></span>
<span data-ttu-id="d37c8-137">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d37c8-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d37c8-138">출력</span><span class="sxs-lookup"><span data-stu-id="d37c8-138">OUTPUTS</span></span>

### <span data-ttu-id="d37c8-139">Microsoft Azure AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d37c8-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="d37c8-140">상속자</span><span class="sxs-lookup"><span data-stu-id="d37c8-140">NOTES</span></span>

## <span data-ttu-id="d37c8-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d37c8-141">RELATED LINKS</span></span>

[<span data-ttu-id="d37c8-142">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d37c8-142">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="d37c8-143">새로운 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d37c8-143">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="d37c8-144">다시 시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d37c8-144">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="d37c8-145">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d37c8-145">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="d37c8-146">시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d37c8-146">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="d37c8-147">중지-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d37c8-147">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="d37c8-148">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="d37c8-148">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
