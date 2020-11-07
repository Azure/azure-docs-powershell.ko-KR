---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restart-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 9f0e48b20d19113290784d65b6bc78531dc7b2a1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876105"
---
# <span data-ttu-id="b0925-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b0925-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="b0925-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0925-102">SYNOPSIS</span></span>

## <span data-ttu-id="b0925-103">구문과</span><span class="sxs-lookup"><span data-stu-id="b0925-103">SYNTAX</span></span>

### <span data-ttu-id="b0925-104">S1</span><span class="sxs-lookup"><span data-stu-id="b0925-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0925-105">구성원과</span><span class="sxs-lookup"><span data-stu-id="b0925-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0925-106">설명은</span><span class="sxs-lookup"><span data-stu-id="b0925-106">DESCRIPTION</span></span>
<span data-ttu-id="b0925-107">**AzWebAppSlot** cmdlet이 중지 된 다음 Azure Web App 슬롯을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0925-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="b0925-108">웹 앱 슬롯이 중지 된 상태 이면 Start-AzWebAppSlot cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0925-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="b0925-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b0925-109">EXAMPLES</span></span>

### <span data-ttu-id="b0925-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b0925-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="b0925-111">이 명령은 리소스 그룹 Default-웹에 연결 된 웹 앱 ContosoWebApp에 대 한 슬롯 Slot001를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0925-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="b0925-112">변수</span><span class="sxs-lookup"><span data-stu-id="b0925-112">PARAMETERS</span></span>

### <span data-ttu-id="b0925-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0925-113">-DefaultProfile</span></span>
<span data-ttu-id="b0925-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0925-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0925-115">-이름</span><span class="sxs-lookup"><span data-stu-id="b0925-115">-Name</span></span>
<span data-ttu-id="b0925-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="b0925-116">WebApp Name</span></span>

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

### <span data-ttu-id="b0925-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0925-117">-ResourceGroupName</span></span>
<span data-ttu-id="b0925-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b0925-118">Resource Group Name</span></span>

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

### <span data-ttu-id="b0925-119">-슬롯</span><span class="sxs-lookup"><span data-stu-id="b0925-119">-Slot</span></span>
<span data-ttu-id="b0925-120">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="b0925-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="b0925-121">-Web app</span><span class="sxs-lookup"><span data-stu-id="b0925-121">-WebApp</span></span>
<span data-ttu-id="b0925-122">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="b0925-122">WebApp Object</span></span>

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

### <span data-ttu-id="b0925-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0925-123">CommonParameters</span></span>
<span data-ttu-id="b0925-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0925-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0925-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0925-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0925-126">입력</span><span class="sxs-lookup"><span data-stu-id="b0925-126">INPUTS</span></span>

### <span data-ttu-id="b0925-127">Site</span><span class="sxs-lookup"><span data-stu-id="b0925-127">Site</span></span>
<span data-ttu-id="b0925-128">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0925-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b0925-129">출력</span><span class="sxs-lookup"><span data-stu-id="b0925-129">OUTPUTS</span></span>

## <span data-ttu-id="b0925-130">상속자</span><span class="sxs-lookup"><span data-stu-id="b0925-130">NOTES</span></span>

## <span data-ttu-id="b0925-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0925-131">RELATED LINKS</span></span>

[<span data-ttu-id="b0925-132">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b0925-132">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="b0925-133">새로운 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b0925-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="b0925-134">제거-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b0925-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="b0925-135">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b0925-135">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="b0925-136">시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b0925-136">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="b0925-137">중지-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b0925-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="b0925-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b0925-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
