---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
ms.openlocfilehash: daacefe94d694a6d6288e4c1ccd0f6b05ad1e582
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530502"
---
# <span data-ttu-id="377f4-101">Get-AzureRmIotHubJob</span><span class="sxs-lookup"><span data-stu-id="377f4-101">Get-AzureRmIotHubJob</span></span>

## <span data-ttu-id="377f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="377f4-102">SYNOPSIS</span></span>
<span data-ttu-id="377f4-103">IotHub 작업에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="377f4-103">Gets the information about an IotHub job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="377f4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="377f4-104">SYNTAX</span></span>

```
Get-AzureRmIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="377f4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="377f4-105">DESCRIPTION</span></span>
<span data-ttu-id="377f4-106">IotHub 작업에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="377f4-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="377f4-107">New-AzureRmIotHubExportDevices 또는 New-AzureRmIotHubImportDevices 명령을 사용 하 여 가져오기 또는 내보내기 작업을 초기에 ted IotHub 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="377f4-107">An IotHub Job gets created when an import or export operation is initialted using the New-AzureRmIotHubExportDevices or New-AzureRmIotHubImportDevices commands.</span></span>
<span data-ttu-id="377f4-108">모든 작업을 나열 하거나 작업 식별자를 기준으로 작업을 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="377f4-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="377f4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="377f4-109">EXAMPLES</span></span>

### <span data-ttu-id="377f4-110">예제 1 모든 작업 나열</span><span class="sxs-lookup"><span data-stu-id="377f4-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="377f4-111">IotHub "myiothub"에 대 한 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="377f4-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="377f4-112">예제 2 특정 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="377f4-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="377f4-113">"Myiothub" IotHub에 대 한 식별자 "3630fc31-4caa-43e8-a232-ea0577221cb2"가 있는 작업에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="377f4-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="377f4-114">변수</span><span class="sxs-lookup"><span data-stu-id="377f4-114">PARAMETERS</span></span>

### <span data-ttu-id="377f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="377f4-115">-DefaultProfile</span></span>
<span data-ttu-id="377f4-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="377f4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="377f4-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="377f4-117">-JobId</span></span>
<span data-ttu-id="377f4-118">작업 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="377f4-118">The Job Identifier.</span></span> 

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

### <span data-ttu-id="377f4-119">-이름</span><span class="sxs-lookup"><span data-stu-id="377f4-119">-Name</span></span>
<span data-ttu-id="377f4-120">IoT hub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="377f4-120">Name of the IoT hub.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="377f4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="377f4-121">-ResourceGroupName</span></span>
<span data-ttu-id="377f4-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="377f4-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="377f4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="377f4-123">CommonParameters</span></span>
<span data-ttu-id="377f4-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="377f4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="377f4-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="377f4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="377f4-126">입력</span><span class="sxs-lookup"><span data-stu-id="377f4-126">INPUTS</span></span>

### <span data-ttu-id="377f4-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="377f4-127">System.String</span></span>

## <span data-ttu-id="377f4-128">출력</span><span class="sxs-lookup"><span data-stu-id="377f4-128">OUTPUTS</span></span>

### <span data-ttu-id="377f4-129">IotHub. PSIotHubJobResponse/. \*</span><span class="sxs-lookup"><span data-stu-id="377f4-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>
<span data-ttu-id="377f4-130">\` \[ \[ PSIotHubJobResponse, IotHub, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = Null 인 경우 목록 1에 있는. a. i a.\]\]</span><span class="sxs-lookup"><span data-stu-id="377f4-130">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="377f4-131">상속자</span><span class="sxs-lookup"><span data-stu-id="377f4-131">NOTES</span></span>

## <span data-ttu-id="377f4-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="377f4-132">RELATED LINKS</span></span>

