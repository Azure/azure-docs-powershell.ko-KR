---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 4bd0e45df7f1c5c98b61f7f490a59a4c305c2c21
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332006"
---
# <span data-ttu-id="9261d-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9261d-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="9261d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9261d-102">SYNOPSIS</span></span>
<span data-ttu-id="9261d-103">Azure 웹앱 슬롯을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9261d-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="9261d-104">구문</span><span class="sxs-lookup"><span data-stu-id="9261d-104">SYNTAX</span></span>

### <span data-ttu-id="9261d-105">S1</span><span class="sxs-lookup"><span data-stu-id="9261d-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9261d-106">S2</span><span class="sxs-lookup"><span data-stu-id="9261d-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9261d-107">설명</span><span class="sxs-lookup"><span data-stu-id="9261d-107">DESCRIPTION</span></span>
<span data-ttu-id="9261d-108">**Get-AzWebAppSlot** cmdlet은 Azure 웹앱 슬롯에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9261d-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="9261d-109">예제</span><span class="sxs-lookup"><span data-stu-id="9261d-109">EXAMPLES</span></span>

### <span data-ttu-id="9261d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="9261d-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="9261d-111">이 명령은 리소스 그룹 Default-Web-WestUS에 속하는 WebAppStandard라는 웹앱에서 Slot001이라는 슬롯을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9261d-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="9261d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9261d-112">PARAMETERS</span></span>

### <span data-ttu-id="9261d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9261d-113">-DefaultProfile</span></span>
<span data-ttu-id="9261d-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9261d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9261d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9261d-115">-Name</span></span>
<span data-ttu-id="9261d-116">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="9261d-116">WebApp Name</span></span>

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

### <span data-ttu-id="9261d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9261d-117">-ResourceGroupName</span></span>
<span data-ttu-id="9261d-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9261d-118">Resource Group Name</span></span>

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

### <span data-ttu-id="9261d-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="9261d-119">-Slot</span></span>
<span data-ttu-id="9261d-120">WebApp 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="9261d-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9261d-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="9261d-121">-WebApp</span></span>
<span data-ttu-id="9261d-122">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="9261d-122">WebApp Object</span></span>

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

### <span data-ttu-id="9261d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9261d-123">CommonParameters</span></span>
<span data-ttu-id="9261d-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9261d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9261d-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9261d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9261d-126">입력</span><span class="sxs-lookup"><span data-stu-id="9261d-126">INPUTS</span></span>

### <span data-ttu-id="9261d-127">System.String</span><span class="sxs-lookup"><span data-stu-id="9261d-127">System.String</span></span>

### <span data-ttu-id="9261d-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="9261d-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9261d-129">출력</span><span class="sxs-lookup"><span data-stu-id="9261d-129">OUTPUTS</span></span>

### <span data-ttu-id="9261d-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="9261d-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9261d-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9261d-131">NOTES</span></span>

## <span data-ttu-id="9261d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9261d-132">RELATED LINKS</span></span>

[<span data-ttu-id="9261d-133">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9261d-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="9261d-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9261d-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="9261d-135">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9261d-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="9261d-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9261d-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="9261d-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9261d-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="9261d-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9261d-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="9261d-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9261d-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
