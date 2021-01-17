---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 88eaf66ea8584913c7816fd12be19509aec49de5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491431"
---
# <span data-ttu-id="2dfd5-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2dfd5-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="2dfd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dfd5-102">SYNOPSIS</span></span>

## <span data-ttu-id="2dfd5-103">구문</span><span class="sxs-lookup"><span data-stu-id="2dfd5-103">SYNTAX</span></span>

### <span data-ttu-id="2dfd5-104">S1</span><span class="sxs-lookup"><span data-stu-id="2dfd5-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dfd5-105">S2</span><span class="sxs-lookup"><span data-stu-id="2dfd5-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dfd5-106">설명</span><span class="sxs-lookup"><span data-stu-id="2dfd5-106">DESCRIPTION</span></span>
<span data-ttu-id="2dfd5-107">**Remove-AzWebAppSlot** cmdlet은 리소스 그룹 및 웹앱 이름을 제공한 Azure 웹앱 슬롯을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2dfd5-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="2dfd5-108">이 cmdlet은 기본적으로 모든 슬롯 및 메트릭도 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2dfd5-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="2dfd5-109">예제</span><span class="sxs-lookup"><span data-stu-id="2dfd5-109">EXAMPLES</span></span>

### <span data-ttu-id="2dfd5-110">예제 1: 웹앱 슬롯 제거</span><span class="sxs-lookup"><span data-stu-id="2dfd5-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="2dfd5-111">이 명령은 Default-Web-WestUS라는 리소스 그룹에 속하는 웹앱 ContosoSite와 연결된 Slot001이라는 슬롯을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2dfd5-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="2dfd5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2dfd5-112">PARAMETERS</span></span>

### <span data-ttu-id="2dfd5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2dfd5-113">-AsJob</span></span>
<span data-ttu-id="2dfd5-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2dfd5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2dfd5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dfd5-115">-DefaultProfile</span></span>
<span data-ttu-id="2dfd5-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2dfd5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dfd5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2dfd5-117">-Force</span></span>
<span data-ttu-id="2dfd5-118">강제로 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="2dfd5-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="2dfd5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2dfd5-119">-Name</span></span>
<span data-ttu-id="2dfd5-120">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="2dfd5-120">WebApp Name</span></span>

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

### <span data-ttu-id="2dfd5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dfd5-121">-ResourceGroupName</span></span>
<span data-ttu-id="2dfd5-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2dfd5-122">Resource Group Name</span></span>

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

### <span data-ttu-id="2dfd5-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="2dfd5-123">-Slot</span></span>
<span data-ttu-id="2dfd5-124">WebApp 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="2dfd5-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="2dfd5-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2dfd5-125">-WebApp</span></span>
<span data-ttu-id="2dfd5-126">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="2dfd5-126">WebApp Object</span></span>

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

### <span data-ttu-id="2dfd5-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2dfd5-127">-Confirm</span></span>
<span data-ttu-id="2dfd5-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2dfd5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dfd5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dfd5-129">-WhatIf</span></span>
<span data-ttu-id="2dfd5-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2dfd5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dfd5-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2dfd5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dfd5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dfd5-132">CommonParameters</span></span>
<span data-ttu-id="2dfd5-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2dfd5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dfd5-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2dfd5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dfd5-135">입력</span><span class="sxs-lookup"><span data-stu-id="2dfd5-135">INPUTS</span></span>

### <span data-ttu-id="2dfd5-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2dfd5-136">System.String</span></span>

### <span data-ttu-id="2dfd5-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="2dfd5-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2dfd5-138">출력</span><span class="sxs-lookup"><span data-stu-id="2dfd5-138">OUTPUTS</span></span>

### <span data-ttu-id="2dfd5-139">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2dfd5-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="2dfd5-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2dfd5-140">NOTES</span></span>

## <span data-ttu-id="2dfd5-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2dfd5-141">RELATED LINKS</span></span>

[<span data-ttu-id="2dfd5-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2dfd5-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="2dfd5-143">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2dfd5-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="2dfd5-144">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2dfd5-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="2dfd5-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2dfd5-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="2dfd5-146">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2dfd5-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="2dfd5-147">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2dfd5-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="2dfd5-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2dfd5-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
