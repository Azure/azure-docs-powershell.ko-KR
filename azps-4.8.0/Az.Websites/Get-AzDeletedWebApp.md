---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: 74c518d4713c19c7a1bb7b7d0b3341e164e22c35
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213131"
---
# <span data-ttu-id="1f2f2-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1f2f2-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="1f2f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f2f2-102">SYNOPSIS</span></span>
<span data-ttu-id="1f2f2-103">구독에서 삭제 된 웹 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f2f2-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="1f2f2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f2f2-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f2f2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1f2f2-105">DESCRIPTION</span></span>
<span data-ttu-id="1f2f2-106">**AzDeletedWebApp** cmdlet은 구독에서 삭제 된 모든 웹 앱을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f2f2-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="1f2f2-107">삭제 된 앱은 리소스 그룹, 이름 및 슬롯을 기준으로 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f2f2-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="1f2f2-108">이름과 리소스 그룹이 같은 삭제 된 앱이 두 개 이상 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f2f2-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="1f2f2-109">DeletionTime에서 같은 이름을 공유 하는 삭제 된 앱을 구분 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f2f2-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="1f2f2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1f2f2-110">EXAMPLES</span></span>

### <span data-ttu-id="1f2f2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1f2f2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="1f2f2-112">이 명령은 리소스 그룹 Default-WestUS에 속한 ContosoSite 이라는 삭제 된 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f2f2-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="1f2f2-113">변수</span><span class="sxs-lookup"><span data-stu-id="1f2f2-113">PARAMETERS</span></span>

### <span data-ttu-id="1f2f2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f2f2-114">-DefaultProfile</span></span>
<span data-ttu-id="1f2f2-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f2f2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f2f2-116">-위치</span><span class="sxs-lookup"><span data-stu-id="1f2f2-116">-Location</span></span>
<span data-ttu-id="1f2f2-117">삭제 된 앱의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="1f2f2-117">The location of the deleted app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f2f2-118">-이름</span><span class="sxs-lookup"><span data-stu-id="1f2f2-118">-Name</span></span>
<span data-ttu-id="1f2f2-119">웹 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f2f2-119">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f2f2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f2f2-120">-ResourceGroupName</span></span>
<span data-ttu-id="1f2f2-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f2f2-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f2f2-122">-슬롯</span><span class="sxs-lookup"><span data-stu-id="1f2f2-122">-Slot</span></span>
<span data-ttu-id="1f2f2-123">웹 앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f2f2-123">The name of the web app slot.</span></span>

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

### <span data-ttu-id="1f2f2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f2f2-124">CommonParameters</span></span>
<span data-ttu-id="1f2f2-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f2f2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f2f2-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f2f2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f2f2-127">입력</span><span class="sxs-lookup"><span data-stu-id="1f2f2-127">INPUTS</span></span>

### <span data-ttu-id="1f2f2-128">않아야</span><span class="sxs-lookup"><span data-stu-id="1f2f2-128">None</span></span>

## <span data-ttu-id="1f2f2-129">출력</span><span class="sxs-lookup"><span data-stu-id="1f2f2-129">OUTPUTS</span></span>

### <span data-ttu-id="1f2f2-130">PSAzureDeletedWebApp (\*). WebApps.</span><span class="sxs-lookup"><span data-stu-id="1f2f2-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="1f2f2-131">상속자</span><span class="sxs-lookup"><span data-stu-id="1f2f2-131">NOTES</span></span>

## <span data-ttu-id="1f2f2-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f2f2-132">RELATED LINKS</span></span>

[<span data-ttu-id="1f2f2-133">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1f2f2-133">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)