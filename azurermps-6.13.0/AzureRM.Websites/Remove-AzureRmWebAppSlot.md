---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: 7fdf5e8de2ec326888c57e8219a006f9ef447aa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530828"
---
# <span data-ttu-id="094e9-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="094e9-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="094e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="094e9-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="094e9-103">구문과</span><span class="sxs-lookup"><span data-stu-id="094e9-103">SYNTAX</span></span>

### <span data-ttu-id="094e9-104">S1</span><span class="sxs-lookup"><span data-stu-id="094e9-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="094e9-105">구성원과</span><span class="sxs-lookup"><span data-stu-id="094e9-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="094e9-106">설명은</span><span class="sxs-lookup"><span data-stu-id="094e9-106">DESCRIPTION</span></span>
<span data-ttu-id="094e9-107">**AzureRmWebAppSlot** cmdlet은 리소스 그룹과 웹 앱 이름을 제공 하는 Azure Web app 슬롯을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="094e9-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="094e9-108">이 cmdlet은 기본적으로 모든 슬롯과 메트릭스도 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="094e9-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="094e9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="094e9-109">EXAMPLES</span></span>

### <span data-ttu-id="094e9-110">예제 1: 웹 앱 슬롯 제거</span><span class="sxs-lookup"><span data-stu-id="094e9-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="094e9-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 웹 앱 ContosoSite와 연결 된 Slot001 이라는 슬롯을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="094e9-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="094e9-112">변수</span><span class="sxs-lookup"><span data-stu-id="094e9-112">PARAMETERS</span></span>

### <span data-ttu-id="094e9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="094e9-113">-AsJob</span></span>
<span data-ttu-id="094e9-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="094e9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="094e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="094e9-115">-DefaultProfile</span></span>
<span data-ttu-id="094e9-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="094e9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="094e9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="094e9-117">-Force</span></span>
<span data-ttu-id="094e9-118">강제로 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="094e9-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="094e9-119">-이름</span><span class="sxs-lookup"><span data-stu-id="094e9-119">-Name</span></span>
<span data-ttu-id="094e9-120">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="094e9-120">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="094e9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="094e9-121">-ResourceGroupName</span></span>
<span data-ttu-id="094e9-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="094e9-122">Resource Group Name</span></span>

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

### <span data-ttu-id="094e9-123">-슬롯</span><span class="sxs-lookup"><span data-stu-id="094e9-123">-Slot</span></span>
<span data-ttu-id="094e9-124">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="094e9-124">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="094e9-125">-Web app</span><span class="sxs-lookup"><span data-stu-id="094e9-125">-WebApp</span></span>
<span data-ttu-id="094e9-126">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="094e9-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="094e9-127">-확인</span><span class="sxs-lookup"><span data-stu-id="094e9-127">-Confirm</span></span>
<span data-ttu-id="094e9-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="094e9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="094e9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="094e9-129">-WhatIf</span></span>
<span data-ttu-id="094e9-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="094e9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="094e9-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="094e9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="094e9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="094e9-132">CommonParameters</span></span>
<span data-ttu-id="094e9-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="094e9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="094e9-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="094e9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="094e9-135">입력</span><span class="sxs-lookup"><span data-stu-id="094e9-135">INPUTS</span></span>

### <span data-ttu-id="094e9-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="094e9-136">System.String</span></span>

### <span data-ttu-id="094e9-137">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="094e9-137">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="094e9-138">매개 변수: Web app (ByValue)</span><span class="sxs-lookup"><span data-stu-id="094e9-138">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="094e9-139">출력</span><span class="sxs-lookup"><span data-stu-id="094e9-139">OUTPUTS</span></span>

### <span data-ttu-id="094e9-140">Microsoft Azure AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="094e9-140">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="094e9-141">상속자</span><span class="sxs-lookup"><span data-stu-id="094e9-141">NOTES</span></span>

## <span data-ttu-id="094e9-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="094e9-142">RELATED LINKS</span></span>

[<span data-ttu-id="094e9-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="094e9-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="094e9-144">새로운 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="094e9-144">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="094e9-145">다시 시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="094e9-145">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="094e9-146">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="094e9-146">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="094e9-147">시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="094e9-147">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="094e9-148">중지-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="094e9-148">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="094e9-149">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="094e9-149">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
