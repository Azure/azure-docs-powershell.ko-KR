---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: 74c518d4713c19c7a1bb7b7d0b3341e164e22c35
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327137"
---
# <span data-ttu-id="a1e60-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="a1e60-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="a1e60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1e60-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e60-103">구독에서 삭제된 웹앱을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a1e60-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="a1e60-104">구문</span><span class="sxs-lookup"><span data-stu-id="a1e60-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1e60-105">설명</span><span class="sxs-lookup"><span data-stu-id="a1e60-105">DESCRIPTION</span></span>
<span data-ttu-id="a1e60-106">**Get-AzDeletedWebApp** cmdlet은 구독에서 삭제된 모든 웹앱을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a1e60-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="a1e60-107">삭제된 앱은 선택적으로 리소스 그룹, 이름 및 슬롯을 통해 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1e60-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="a1e60-108">동일한 이름 및 리소스 그룹을 사용하여 삭제된 앱이 두 개 이상 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1e60-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="a1e60-109">동일한 이름을 공유하는 삭제된 앱을 구분하려면 DeletionTime을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="a1e60-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="a1e60-110">예제</span><span class="sxs-lookup"><span data-stu-id="a1e60-110">EXAMPLES</span></span>

### <span data-ttu-id="a1e60-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a1e60-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="a1e60-112">이 명령은 리소스 그룹 Default-Web-WestUS에 속하는 ContosoSite라는 삭제된 앱을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a1e60-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a1e60-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1e60-113">PARAMETERS</span></span>

### <span data-ttu-id="a1e60-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1e60-114">-DefaultProfile</span></span>
<span data-ttu-id="a1e60-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a1e60-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1e60-116">-Location</span><span class="sxs-lookup"><span data-stu-id="a1e60-116">-Location</span></span>
<span data-ttu-id="a1e60-117">삭제된 앱의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a1e60-117">The location of the deleted app.</span></span>

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

### <span data-ttu-id="a1e60-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a1e60-118">-Name</span></span>
<span data-ttu-id="a1e60-119">웹앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a1e60-119">The name of the web app.</span></span>

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

### <span data-ttu-id="a1e60-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1e60-120">-ResourceGroupName</span></span>
<span data-ttu-id="a1e60-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a1e60-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="a1e60-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="a1e60-122">-Slot</span></span>
<span data-ttu-id="a1e60-123">웹앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a1e60-123">The name of the web app slot.</span></span>

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

### <span data-ttu-id="a1e60-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e60-124">CommonParameters</span></span>
<span data-ttu-id="a1e60-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a1e60-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e60-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a1e60-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e60-127">입력</span><span class="sxs-lookup"><span data-stu-id="a1e60-127">INPUTS</span></span>

### <span data-ttu-id="a1e60-128">없음</span><span class="sxs-lookup"><span data-stu-id="a1e60-128">None</span></span>

## <span data-ttu-id="a1e60-129">출력</span><span class="sxs-lookup"><span data-stu-id="a1e60-129">OUTPUTS</span></span>

### <span data-ttu-id="a1e60-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="a1e60-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="a1e60-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a1e60-131">NOTES</span></span>

## <span data-ttu-id="a1e60-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a1e60-132">RELATED LINKS</span></span>

[<span data-ttu-id="a1e60-133">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="a1e60-133">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)