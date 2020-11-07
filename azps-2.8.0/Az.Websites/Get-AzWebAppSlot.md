---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 4d8091c4335bbba9574c112675bd4bdbbcaea662
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874455"
---
# <span data-ttu-id="9567b-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9567b-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="9567b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9567b-102">SYNOPSIS</span></span>
<span data-ttu-id="9567b-103">Azure 웹 앱 슬롯을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9567b-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="9567b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9567b-104">SYNTAX</span></span>

### <span data-ttu-id="9567b-105">S1</span><span class="sxs-lookup"><span data-stu-id="9567b-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9567b-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="9567b-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9567b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9567b-107">DESCRIPTION</span></span>
<span data-ttu-id="9567b-108">**AzWebAppSlot** Cmdlet은 Azure Web App 슬롯에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9567b-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="9567b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9567b-109">EXAMPLES</span></span>

### <span data-ttu-id="9567b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="9567b-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="9567b-111">이 명령은 리소스 그룹 Default-웹용 WestUS에 속한 WebAppStandard 라는 웹 앱에서 Slot001 라는 슬롯을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9567b-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="9567b-112">변수</span><span class="sxs-lookup"><span data-stu-id="9567b-112">PARAMETERS</span></span>

### <span data-ttu-id="9567b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9567b-113">-DefaultProfile</span></span>
<span data-ttu-id="9567b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9567b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9567b-115">-이름</span><span class="sxs-lookup"><span data-stu-id="9567b-115">-Name</span></span>
<span data-ttu-id="9567b-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="9567b-116">WebApp Name</span></span>

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

### <span data-ttu-id="9567b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9567b-117">-ResourceGroupName</span></span>
<span data-ttu-id="9567b-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9567b-118">Resource Group Name</span></span>

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

### <span data-ttu-id="9567b-119">-슬롯</span><span class="sxs-lookup"><span data-stu-id="9567b-119">-Slot</span></span>
<span data-ttu-id="9567b-120">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="9567b-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="9567b-121">-Web app</span><span class="sxs-lookup"><span data-stu-id="9567b-121">-WebApp</span></span>
<span data-ttu-id="9567b-122">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="9567b-122">WebApp Object</span></span>

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

### <span data-ttu-id="9567b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9567b-123">CommonParameters</span></span>
<span data-ttu-id="9567b-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9567b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9567b-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9567b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9567b-126">입력</span><span class="sxs-lookup"><span data-stu-id="9567b-126">INPUTS</span></span>

### <span data-ttu-id="9567b-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9567b-127">System.String</span></span>

### <span data-ttu-id="9567b-128">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="9567b-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9567b-129">출력</span><span class="sxs-lookup"><span data-stu-id="9567b-129">OUTPUTS</span></span>

### <span data-ttu-id="9567b-130">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="9567b-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9567b-131">상속자</span><span class="sxs-lookup"><span data-stu-id="9567b-131">NOTES</span></span>

## <span data-ttu-id="9567b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9567b-132">RELATED LINKS</span></span>

[<span data-ttu-id="9567b-133">새로운 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9567b-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="9567b-134">제거-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9567b-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="9567b-135">다시 시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9567b-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="9567b-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9567b-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="9567b-137">시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9567b-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="9567b-138">중지-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9567b-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="9567b-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9567b-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
