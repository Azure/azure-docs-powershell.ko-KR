---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
ms.openlocfilehash: 7c5c09f2379eb1c0306b89018732336b4223f5c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303989"
---
# <span data-ttu-id="a10de-101">Get-AzIotHubJob</span><span class="sxs-lookup"><span data-stu-id="a10de-101">Get-AzIotHubJob</span></span>

## <span data-ttu-id="a10de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a10de-102">SYNOPSIS</span></span>
<span data-ttu-id="a10de-103">IotHub 작업에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a10de-103">Gets the information about an IotHub job.</span></span>

## <span data-ttu-id="a10de-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a10de-104">SYNTAX</span></span>

```
Get-AzIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a10de-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a10de-105">DESCRIPTION</span></span>
<span data-ttu-id="a10de-106">IotHub 작업에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a10de-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="a10de-107">New-AzIotHubExportDevices 또는 New-AzIotHubImportDevices 명령을 사용 하 여 가져오기 또는 내보내기 작업을 초기화할 때 IotHub 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a10de-107">An IotHub Job gets created when an import or export operation is initialized using the New-AzIotHubExportDevices or New-AzIotHubImportDevices commands.</span></span>
<span data-ttu-id="a10de-108">모든 작업을 나열 하거나 작업 식별자를 기준으로 작업을 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a10de-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="a10de-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a10de-109">EXAMPLES</span></span>

### <span data-ttu-id="a10de-110">예제 1 모든 작업 나열</span><span class="sxs-lookup"><span data-stu-id="a10de-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="a10de-111">IotHub "myiothub"에 대 한 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a10de-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="a10de-112">예제 2 특정 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="a10de-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="a10de-113">"Myiothub" IotHub에 대 한 식별자 "3630fc31-4caa-43e8-a232-ea0577221cb2"가 있는 작업에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a10de-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="a10de-114">변수</span><span class="sxs-lookup"><span data-stu-id="a10de-114">PARAMETERS</span></span>

### <span data-ttu-id="a10de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a10de-115">-DefaultProfile</span></span>
<span data-ttu-id="a10de-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a10de-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a10de-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="a10de-117">-JobId</span></span>
<span data-ttu-id="a10de-118">작업 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a10de-118">The Job Identifier.</span></span> 

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

### <span data-ttu-id="a10de-119">-이름</span><span class="sxs-lookup"><span data-stu-id="a10de-119">-Name</span></span>
<span data-ttu-id="a10de-120">IoT hub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a10de-120">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a10de-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a10de-121">-ResourceGroupName</span></span>
<span data-ttu-id="a10de-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="a10de-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a10de-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a10de-123">CommonParameters</span></span>
<span data-ttu-id="a10de-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a10de-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a10de-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a10de-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a10de-126">입력</span><span class="sxs-lookup"><span data-stu-id="a10de-126">INPUTS</span></span>

### <span data-ttu-id="a10de-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a10de-127">System.String</span></span>

## <span data-ttu-id="a10de-128">출력</span><span class="sxs-lookup"><span data-stu-id="a10de-128">OUTPUTS</span></span>

### <span data-ttu-id="a10de-129">IotHub. PSIotHubJobResponse/. \*</span><span class="sxs-lookup"><span data-stu-id="a10de-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="a10de-130">상속자</span><span class="sxs-lookup"><span data-stu-id="a10de-130">NOTES</span></span>

## <span data-ttu-id="a10de-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a10de-131">RELATED LINKS</span></span>
