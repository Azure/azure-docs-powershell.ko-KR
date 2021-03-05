---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/powershell/module/az.websites/restart-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 75bedf4546bee73767c0488f578cdb5e17c1b745
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002080"
---
# <span data-ttu-id="1a594-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1a594-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="1a594-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a594-102">SYNOPSIS</span></span>

## <span data-ttu-id="1a594-103">구문</span><span class="sxs-lookup"><span data-stu-id="1a594-103">SYNTAX</span></span>

### <span data-ttu-id="1a594-104">S1</span><span class="sxs-lookup"><span data-stu-id="1a594-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a594-105">S2</span><span class="sxs-lookup"><span data-stu-id="1a594-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a594-106">설명</span><span class="sxs-lookup"><span data-stu-id="1a594-106">DESCRIPTION</span></span>
<span data-ttu-id="1a594-107">**다시 시작-AzWebAppSlot cmdlet이** 중지된 다음 Azure Web App Slot을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="1a594-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="1a594-108">웹앱 슬롯이 중지된 상태인 경우 Start-AzWebAppSlot cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="1a594-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="1a594-109">예제</span><span class="sxs-lookup"><span data-stu-id="1a594-109">EXAMPLES</span></span>

### <span data-ttu-id="1a594-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1a594-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="1a594-111">이 명령은 리소스 그룹 Default-Web-WestUS와 연결된 웹앱 ContosoWebApp에 대한 슬롯 슬롯001을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="1a594-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="1a594-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1a594-112">PARAMETERS</span></span>

### <span data-ttu-id="1a594-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a594-113">-DefaultProfile</span></span>
<span data-ttu-id="1a594-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a594-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a594-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1a594-115">-Name</span></span>
<span data-ttu-id="1a594-116">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="1a594-116">WebApp Name</span></span>

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

### <span data-ttu-id="1a594-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a594-117">-ResourceGroupName</span></span>
<span data-ttu-id="1a594-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1a594-118">Resource Group Name</span></span>

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

### <span data-ttu-id="1a594-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="1a594-119">-Slot</span></span>
<span data-ttu-id="1a594-120">WebApp 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="1a594-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="1a594-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1a594-121">-WebApp</span></span>
<span data-ttu-id="1a594-122">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="1a594-122">WebApp Object</span></span>

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

### <span data-ttu-id="1a594-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a594-123">CommonParameters</span></span>
<span data-ttu-id="1a594-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1a594-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a594-125">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1a594-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a594-126">입력</span><span class="sxs-lookup"><span data-stu-id="1a594-126">INPUTS</span></span>

### <span data-ttu-id="1a594-127">System.String</span><span class="sxs-lookup"><span data-stu-id="1a594-127">System.String</span></span>

### <span data-ttu-id="1a594-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="1a594-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1a594-129">출력</span><span class="sxs-lookup"><span data-stu-id="1a594-129">OUTPUTS</span></span>

### <span data-ttu-id="1a594-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="1a594-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1a594-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1a594-131">NOTES</span></span>

## <span data-ttu-id="1a594-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a594-132">RELATED LINKS</span></span>

[<span data-ttu-id="1a594-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1a594-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="1a594-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1a594-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="1a594-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1a594-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="1a594-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1a594-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="1a594-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1a594-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="1a594-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1a594-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="1a594-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1a594-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
