---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 4bd0e45df7f1c5c98b61f7f490a59a4c305c2c21
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215735"
---
# <span data-ttu-id="7871a-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7871a-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="7871a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7871a-102">SYNOPSIS</span></span>
<span data-ttu-id="7871a-103">Azure 웹 앱 슬롯을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7871a-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="7871a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7871a-104">SYNTAX</span></span>

### <span data-ttu-id="7871a-105">S1</span><span class="sxs-lookup"><span data-stu-id="7871a-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7871a-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="7871a-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7871a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7871a-107">DESCRIPTION</span></span>
<span data-ttu-id="7871a-108">**AzWebAppSlot** Cmdlet은 Azure Web App 슬롯에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7871a-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="7871a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7871a-109">EXAMPLES</span></span>

### <span data-ttu-id="7871a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7871a-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="7871a-111">이 명령은 리소스 그룹 Default-웹용 WestUS에 속한 WebAppStandard 라는 웹 앱에서 Slot001 라는 슬롯을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7871a-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="7871a-112">변수</span><span class="sxs-lookup"><span data-stu-id="7871a-112">PARAMETERS</span></span>

### <span data-ttu-id="7871a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7871a-113">-DefaultProfile</span></span>
<span data-ttu-id="7871a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7871a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7871a-115">-이름</span><span class="sxs-lookup"><span data-stu-id="7871a-115">-Name</span></span>
<span data-ttu-id="7871a-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="7871a-116">WebApp Name</span></span>

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

### <span data-ttu-id="7871a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7871a-117">-ResourceGroupName</span></span>
<span data-ttu-id="7871a-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7871a-118">Resource Group Name</span></span>

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

### <span data-ttu-id="7871a-119">-슬롯</span><span class="sxs-lookup"><span data-stu-id="7871a-119">-Slot</span></span>
<span data-ttu-id="7871a-120">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="7871a-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="7871a-121">-Web app</span><span class="sxs-lookup"><span data-stu-id="7871a-121">-WebApp</span></span>
<span data-ttu-id="7871a-122">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="7871a-122">WebApp Object</span></span>

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

### <span data-ttu-id="7871a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7871a-123">CommonParameters</span></span>
<span data-ttu-id="7871a-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7871a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7871a-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7871a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7871a-126">입력</span><span class="sxs-lookup"><span data-stu-id="7871a-126">INPUTS</span></span>

### <span data-ttu-id="7871a-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7871a-127">System.String</span></span>

### <span data-ttu-id="7871a-128">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="7871a-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7871a-129">출력</span><span class="sxs-lookup"><span data-stu-id="7871a-129">OUTPUTS</span></span>

### <span data-ttu-id="7871a-130">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="7871a-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7871a-131">상속자</span><span class="sxs-lookup"><span data-stu-id="7871a-131">NOTES</span></span>

## <span data-ttu-id="7871a-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7871a-132">RELATED LINKS</span></span>

[<span data-ttu-id="7871a-133">새로운 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7871a-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="7871a-134">제거-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7871a-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="7871a-135">다시 시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7871a-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="7871a-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7871a-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="7871a-137">시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7871a-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="7871a-138">중지-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7871a-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="7871a-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7871a-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
