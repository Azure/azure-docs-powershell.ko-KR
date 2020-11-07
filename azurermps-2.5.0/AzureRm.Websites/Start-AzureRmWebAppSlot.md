---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 97bf4078ca09ce250fea0d7c660629fbab651974
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882089"
---
# <span data-ttu-id="ee200-101">Start-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ee200-101">Start-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="ee200-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee200-102">SYNOPSIS</span></span>
<span data-ttu-id="ee200-103">Azure Web App 슬롯을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee200-103">Starts an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee200-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ee200-104">SYNTAX</span></span>

### <span data-ttu-id="ee200-105">S1</span><span class="sxs-lookup"><span data-stu-id="ee200-105">S1</span></span>
```
Start-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee200-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="ee200-106">S2</span></span>
```
Start-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee200-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ee200-107">DESCRIPTION</span></span>
<span data-ttu-id="ee200-108">**AzureRmWebAppSlot** Cmdlet은 Azure Web App 슬롯을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee200-108">The **Start-AzureRmWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="ee200-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ee200-109">EXAMPLES</span></span>

### <span data-ttu-id="ee200-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ee200-110">Example 1</span></span>
```
PS C:\>Start-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="ee200-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoWebApp 이라는 웹 앱에 대 한 Slot001 이라는 슬롯을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee200-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ee200-112">변수</span><span class="sxs-lookup"><span data-stu-id="ee200-112">PARAMETERS</span></span>

### <span data-ttu-id="ee200-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee200-113">-DefaultProfile</span></span>
<span data-ttu-id="ee200-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee200-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee200-115">-이름</span><span class="sxs-lookup"><span data-stu-id="ee200-115">-Name</span></span>
<span data-ttu-id="ee200-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="ee200-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee200-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee200-117">-ResourceGroupName</span></span>
<span data-ttu-id="ee200-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ee200-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee200-119">-슬롯</span><span class="sxs-lookup"><span data-stu-id="ee200-119">-Slot</span></span>
<span data-ttu-id="ee200-120">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="ee200-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee200-121">-Web app</span><span class="sxs-lookup"><span data-stu-id="ee200-121">-WebApp</span></span>
<span data-ttu-id="ee200-122">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="ee200-122">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee200-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee200-123">CommonParameters</span></span>
<span data-ttu-id="ee200-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee200-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee200-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee200-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee200-126">입력</span><span class="sxs-lookup"><span data-stu-id="ee200-126">INPUTS</span></span>

### <span data-ttu-id="ee200-127">Site</span><span class="sxs-lookup"><span data-stu-id="ee200-127">Site</span></span>
<span data-ttu-id="ee200-128">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee200-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ee200-129">출력</span><span class="sxs-lookup"><span data-stu-id="ee200-129">OUTPUTS</span></span>

## <span data-ttu-id="ee200-130">상속자</span><span class="sxs-lookup"><span data-stu-id="ee200-130">NOTES</span></span>

## <span data-ttu-id="ee200-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee200-131">RELATED LINKS</span></span>

[<span data-ttu-id="ee200-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ee200-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="ee200-133">새로운 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ee200-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="ee200-134">제거-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ee200-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="ee200-135">다시 시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ee200-135">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="ee200-136">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ee200-136">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="ee200-137">중지-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ee200-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="ee200-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ee200-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
