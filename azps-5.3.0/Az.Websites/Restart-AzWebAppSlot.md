---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 377e08f344256f6d744fec66f0b6b20f495d9309
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491425"
---
# <span data-ttu-id="44b9e-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44b9e-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="44b9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44b9e-102">SYNOPSIS</span></span>

## <span data-ttu-id="44b9e-103">구문</span><span class="sxs-lookup"><span data-stu-id="44b9e-103">SYNTAX</span></span>

### <span data-ttu-id="44b9e-104">S1</span><span class="sxs-lookup"><span data-stu-id="44b9e-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44b9e-105">S2</span><span class="sxs-lookup"><span data-stu-id="44b9e-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44b9e-106">설명</span><span class="sxs-lookup"><span data-stu-id="44b9e-106">DESCRIPTION</span></span>
<span data-ttu-id="44b9e-107">**Restart-AzWebAppSlot** cmdlet이 중지된 다음 Azure 웹앱 슬롯을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="44b9e-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="44b9e-108">웹앱 슬롯이 중지된 상태인 경우 Start-AzWebAppSlot cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="44b9e-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="44b9e-109">예제</span><span class="sxs-lookup"><span data-stu-id="44b9e-109">EXAMPLES</span></span>

### <span data-ttu-id="44b9e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="44b9e-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="44b9e-111">이 명령은 리소스 그룹 Default-Web-WestUS와 연결된 웹앱 ContosoWebApp에 대한 Slot001을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="44b9e-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="44b9e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44b9e-112">PARAMETERS</span></span>

### <span data-ttu-id="44b9e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44b9e-113">-DefaultProfile</span></span>
<span data-ttu-id="44b9e-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44b9e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44b9e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="44b9e-115">-Name</span></span>
<span data-ttu-id="44b9e-116">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="44b9e-116">WebApp Name</span></span>

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

### <span data-ttu-id="44b9e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44b9e-117">-ResourceGroupName</span></span>
<span data-ttu-id="44b9e-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="44b9e-118">Resource Group Name</span></span>

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

### <span data-ttu-id="44b9e-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="44b9e-119">-Slot</span></span>
<span data-ttu-id="44b9e-120">WebApp 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="44b9e-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="44b9e-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="44b9e-121">-WebApp</span></span>
<span data-ttu-id="44b9e-122">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="44b9e-122">WebApp Object</span></span>

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

### <span data-ttu-id="44b9e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44b9e-123">CommonParameters</span></span>
<span data-ttu-id="44b9e-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="44b9e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44b9e-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="44b9e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44b9e-126">입력</span><span class="sxs-lookup"><span data-stu-id="44b9e-126">INPUTS</span></span>

### <span data-ttu-id="44b9e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="44b9e-127">System.String</span></span>

### <span data-ttu-id="44b9e-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="44b9e-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="44b9e-129">출력</span><span class="sxs-lookup"><span data-stu-id="44b9e-129">OUTPUTS</span></span>

### <span data-ttu-id="44b9e-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="44b9e-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="44b9e-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="44b9e-131">NOTES</span></span>

## <span data-ttu-id="44b9e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44b9e-132">RELATED LINKS</span></span>

[<span data-ttu-id="44b9e-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44b9e-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="44b9e-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44b9e-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="44b9e-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44b9e-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="44b9e-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44b9e-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="44b9e-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44b9e-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="44b9e-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44b9e-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="44b9e-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="44b9e-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
