---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmDeletedWebApp.md
ms.openlocfilehash: 75ad4e1fabb511ee4ca3cff024389a8e826aeadd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530831"
---
# <span data-ttu-id="3426e-101">Get-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="3426e-101">Get-AzureRmDeletedWebApp</span></span>

## <span data-ttu-id="3426e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3426e-102">SYNOPSIS</span></span>
<span data-ttu-id="3426e-103">구독에서 삭제 된 웹 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3426e-103">Gets deleted web apps in the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3426e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3426e-104">SYNTAX</span></span>

```
Get-AzureRmDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3426e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3426e-105">DESCRIPTION</span></span>
<span data-ttu-id="3426e-106">**AzureRmDeletedWebApp** cmdlet은 구독에서 삭제 된 모든 웹 앱을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3426e-106">The **Get-AzureRmDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="3426e-107">삭제 된 앱은 리소스 그룹, 이름 및 슬롯을 기준으로 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3426e-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="3426e-108">이름과 리소스 그룹이 같은 삭제 된 앱이 두 개 이상 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3426e-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="3426e-109">DeletionTime에서 같은 이름을 공유 하는 삭제 된 앱을 구분 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3426e-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="3426e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3426e-110">EXAMPLES</span></span>

### <span data-ttu-id="3426e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3426e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="3426e-112">이 명령은 리소스 그룹 Default-WestUS에 속한 ContosoSite 이라는 삭제 된 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3426e-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="3426e-113">변수</span><span class="sxs-lookup"><span data-stu-id="3426e-113">PARAMETERS</span></span>

### <span data-ttu-id="3426e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3426e-114">-DefaultProfile</span></span>
<span data-ttu-id="3426e-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3426e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3426e-116">-이름</span><span class="sxs-lookup"><span data-stu-id="3426e-116">-Name</span></span>
<span data-ttu-id="3426e-117">웹 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3426e-117">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3426e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3426e-118">-ResourceGroupName</span></span>
<span data-ttu-id="3426e-119">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3426e-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3426e-120">-슬롯</span><span class="sxs-lookup"><span data-stu-id="3426e-120">-Slot</span></span>
<span data-ttu-id="3426e-121">웹 앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3426e-121">The name of the web app slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3426e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3426e-122">CommonParameters</span></span>
<span data-ttu-id="3426e-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3426e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3426e-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3426e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3426e-125">입력</span><span class="sxs-lookup"><span data-stu-id="3426e-125">INPUTS</span></span>

### <span data-ttu-id="3426e-126">않아야</span><span class="sxs-lookup"><span data-stu-id="3426e-126">None</span></span>

## <span data-ttu-id="3426e-127">출력</span><span class="sxs-lookup"><span data-stu-id="3426e-127">OUTPUTS</span></span>

### <span data-ttu-id="3426e-128">PSAzureDeletedWebApp (\*). WebApps.</span><span class="sxs-lookup"><span data-stu-id="3426e-128">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="3426e-129">상속자</span><span class="sxs-lookup"><span data-stu-id="3426e-129">NOTES</span></span>

## <span data-ttu-id="3426e-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3426e-130">RELATED LINKS</span></span>

[<span data-ttu-id="3426e-131">Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="3426e-131">Restore-AzureRmDeletedWebApp</span></span>](./Restore-AzureRmDeletedWebApp.md)
