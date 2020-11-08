---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 377e08f344256f6d744fec66f0b6b20f495d9309
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217954"
---
# <span data-ttu-id="c1a67-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c1a67-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="c1a67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1a67-102">SYNOPSIS</span></span>

## <span data-ttu-id="c1a67-103">구문과</span><span class="sxs-lookup"><span data-stu-id="c1a67-103">SYNTAX</span></span>

### <span data-ttu-id="c1a67-104">S1</span><span class="sxs-lookup"><span data-stu-id="c1a67-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1a67-105">구성원과</span><span class="sxs-lookup"><span data-stu-id="c1a67-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1a67-106">설명은</span><span class="sxs-lookup"><span data-stu-id="c1a67-106">DESCRIPTION</span></span>
<span data-ttu-id="c1a67-107">**AzWebAppSlot** cmdlet이 중지 된 다음 Azure Web App 슬롯을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1a67-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="c1a67-108">웹 앱 슬롯이 중지 된 상태 이면 Start-AzWebAppSlot cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1a67-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="c1a67-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c1a67-109">EXAMPLES</span></span>

### <span data-ttu-id="c1a67-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c1a67-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="c1a67-111">이 명령은 리소스 그룹 Default-웹에 연결 된 웹 앱 ContosoWebApp에 대 한 슬롯 Slot001를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1a67-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="c1a67-112">변수</span><span class="sxs-lookup"><span data-stu-id="c1a67-112">PARAMETERS</span></span>

### <span data-ttu-id="c1a67-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1a67-113">-DefaultProfile</span></span>
<span data-ttu-id="c1a67-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c1a67-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1a67-115">-이름</span><span class="sxs-lookup"><span data-stu-id="c1a67-115">-Name</span></span>
<span data-ttu-id="c1a67-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="c1a67-116">WebApp Name</span></span>

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

### <span data-ttu-id="c1a67-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1a67-117">-ResourceGroupName</span></span>
<span data-ttu-id="c1a67-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c1a67-118">Resource Group Name</span></span>

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

### <span data-ttu-id="c1a67-119">-슬롯</span><span class="sxs-lookup"><span data-stu-id="c1a67-119">-Slot</span></span>
<span data-ttu-id="c1a67-120">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="c1a67-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="c1a67-121">-Web app</span><span class="sxs-lookup"><span data-stu-id="c1a67-121">-WebApp</span></span>
<span data-ttu-id="c1a67-122">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="c1a67-122">WebApp Object</span></span>

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

### <span data-ttu-id="c1a67-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1a67-123">CommonParameters</span></span>
<span data-ttu-id="c1a67-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1a67-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1a67-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1a67-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1a67-126">입력</span><span class="sxs-lookup"><span data-stu-id="c1a67-126">INPUTS</span></span>

### <span data-ttu-id="c1a67-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c1a67-127">System.String</span></span>

### <span data-ttu-id="c1a67-128">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="c1a67-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c1a67-129">출력</span><span class="sxs-lookup"><span data-stu-id="c1a67-129">OUTPUTS</span></span>

### <span data-ttu-id="c1a67-130">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="c1a67-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c1a67-131">상속자</span><span class="sxs-lookup"><span data-stu-id="c1a67-131">NOTES</span></span>

## <span data-ttu-id="c1a67-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1a67-132">RELATED LINKS</span></span>

[<span data-ttu-id="c1a67-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c1a67-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="c1a67-134">새로운 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c1a67-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="c1a67-135">제거-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c1a67-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="c1a67-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c1a67-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="c1a67-137">시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c1a67-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="c1a67-138">중지-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c1a67-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="c1a67-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c1a67-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
