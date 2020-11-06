---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
ms.openlocfilehash: ace1b16bc6d89fb619daba23a214326acd8d0d24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525448"
---
# <span data-ttu-id="4863d-101">Restart-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4863d-101">Restart-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="4863d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4863d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4863d-103">구문과</span><span class="sxs-lookup"><span data-stu-id="4863d-103">SYNTAX</span></span>

### <span data-ttu-id="4863d-104">S1</span><span class="sxs-lookup"><span data-stu-id="4863d-104">S1</span></span>
```
Restart-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4863d-105">구성원과</span><span class="sxs-lookup"><span data-stu-id="4863d-105">S2</span></span>
```
Restart-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4863d-106">설명은</span><span class="sxs-lookup"><span data-stu-id="4863d-106">DESCRIPTION</span></span>
<span data-ttu-id="4863d-107">**AzureRmWebAppSlot** cmdlet이 중지 된 다음 Azure Web App 슬롯을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="4863d-107">The **Restart-AzureRmWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="4863d-108">웹 앱 슬롯이 중지 된 상태 이면 Start-AzureRmWebAppSlot cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4863d-108">If the Web App Slot is in a stopped state, use the Start-AzureRmWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="4863d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4863d-109">EXAMPLES</span></span>

### <span data-ttu-id="4863d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4863d-110">Example 1</span></span>
```
PS C:\> Restart-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="4863d-111">이 명령은 리소스 그룹 Default-웹에 연결 된 웹 앱 ContosoWebApp에 대 한 슬롯 Slot001를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="4863d-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="4863d-112">변수</span><span class="sxs-lookup"><span data-stu-id="4863d-112">PARAMETERS</span></span>

### <span data-ttu-id="4863d-113">-이름</span><span class="sxs-lookup"><span data-stu-id="4863d-113">-Name</span></span>
<span data-ttu-id="4863d-114">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="4863d-114">WebApp Name</span></span>

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

### <span data-ttu-id="4863d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4863d-115">-ResourceGroupName</span></span>
<span data-ttu-id="4863d-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4863d-116">Resource Group Name</span></span>

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

### <span data-ttu-id="4863d-117">-슬롯</span><span class="sxs-lookup"><span data-stu-id="4863d-117">-Slot</span></span>
<span data-ttu-id="4863d-118">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="4863d-118">WebApp Slot Name</span></span>

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

### <span data-ttu-id="4863d-119">-Web app</span><span class="sxs-lookup"><span data-stu-id="4863d-119">-WebApp</span></span>
<span data-ttu-id="4863d-120">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="4863d-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4863d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4863d-121">-DefaultProfile</span></span>
<span data-ttu-id="4863d-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4863d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4863d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4863d-123">CommonParameters</span></span>
<span data-ttu-id="4863d-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4863d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4863d-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4863d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4863d-126">입력</span><span class="sxs-lookup"><span data-stu-id="4863d-126">INPUTS</span></span>

### <span data-ttu-id="4863d-127">Site</span><span class="sxs-lookup"><span data-stu-id="4863d-127">Site</span></span>
<span data-ttu-id="4863d-128">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4863d-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="4863d-129">출력</span><span class="sxs-lookup"><span data-stu-id="4863d-129">OUTPUTS</span></span>

## <span data-ttu-id="4863d-130">상속자</span><span class="sxs-lookup"><span data-stu-id="4863d-130">NOTES</span></span>

## <span data-ttu-id="4863d-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4863d-131">RELATED LINKS</span></span>

[<span data-ttu-id="4863d-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4863d-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="4863d-133">새로운 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4863d-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="4863d-134">제거-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4863d-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="4863d-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4863d-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="4863d-136">시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4863d-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="4863d-137">중지-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4863d-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="4863d-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4863d-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
