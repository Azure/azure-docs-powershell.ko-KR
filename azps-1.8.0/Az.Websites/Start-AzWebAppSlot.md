---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: 0535eee5dcdc3d0e78f95951fddcca9d7b8fff3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698286"
---
# <span data-ttu-id="ec72d-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ec72d-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="ec72d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec72d-102">SYNOPSIS</span></span>
<span data-ttu-id="ec72d-103">Azure Web App 슬롯을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec72d-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="ec72d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ec72d-104">SYNTAX</span></span>

### <span data-ttu-id="ec72d-105">S1</span><span class="sxs-lookup"><span data-stu-id="ec72d-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec72d-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="ec72d-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec72d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ec72d-107">DESCRIPTION</span></span>
<span data-ttu-id="ec72d-108">**AzWebAppSlot** Cmdlet은 Azure Web App 슬롯을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec72d-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="ec72d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ec72d-109">EXAMPLES</span></span>

### <span data-ttu-id="ec72d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ec72d-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="ec72d-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoWebApp 이라는 웹 앱에 대 한 Slot001 이라는 슬롯을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec72d-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ec72d-112">변수</span><span class="sxs-lookup"><span data-stu-id="ec72d-112">PARAMETERS</span></span>

### <span data-ttu-id="ec72d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec72d-113">-DefaultProfile</span></span>
<span data-ttu-id="ec72d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec72d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec72d-115">-이름</span><span class="sxs-lookup"><span data-stu-id="ec72d-115">-Name</span></span>
<span data-ttu-id="ec72d-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="ec72d-116">WebApp Name</span></span>

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

### <span data-ttu-id="ec72d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec72d-117">-ResourceGroupName</span></span>
<span data-ttu-id="ec72d-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ec72d-118">Resource Group Name</span></span>

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

### <span data-ttu-id="ec72d-119">-슬롯</span><span class="sxs-lookup"><span data-stu-id="ec72d-119">-Slot</span></span>
<span data-ttu-id="ec72d-120">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="ec72d-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="ec72d-121">-Web app</span><span class="sxs-lookup"><span data-stu-id="ec72d-121">-WebApp</span></span>
<span data-ttu-id="ec72d-122">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="ec72d-122">WebApp Object</span></span>

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

### <span data-ttu-id="ec72d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec72d-123">CommonParameters</span></span>
<span data-ttu-id="ec72d-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec72d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec72d-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec72d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec72d-126">입력</span><span class="sxs-lookup"><span data-stu-id="ec72d-126">INPUTS</span></span>

### <span data-ttu-id="ec72d-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ec72d-127">System.String</span></span>

### <span data-ttu-id="ec72d-128">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="ec72d-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ec72d-129">출력</span><span class="sxs-lookup"><span data-stu-id="ec72d-129">OUTPUTS</span></span>

### <span data-ttu-id="ec72d-130">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="ec72d-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ec72d-131">상속자</span><span class="sxs-lookup"><span data-stu-id="ec72d-131">NOTES</span></span>

## <span data-ttu-id="ec72d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec72d-132">RELATED LINKS</span></span>

[<span data-ttu-id="ec72d-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ec72d-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="ec72d-134">새로운 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ec72d-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="ec72d-135">제거-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ec72d-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="ec72d-136">다시 시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ec72d-136">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="ec72d-137">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ec72d-137">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="ec72d-138">중지-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ec72d-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="ec72d-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ec72d-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
