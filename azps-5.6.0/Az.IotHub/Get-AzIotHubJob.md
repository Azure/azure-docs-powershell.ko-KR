---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
ms.openlocfilehash: 191b5a75a5f9f581308c8d5aa214fe4f2ae84851
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987980"
---
# <span data-ttu-id="82d38-101">Get-AzIotHubJob</span><span class="sxs-lookup"><span data-stu-id="82d38-101">Get-AzIotHubJob</span></span>

## <span data-ttu-id="82d38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82d38-102">SYNOPSIS</span></span>
<span data-ttu-id="82d38-103">IotHub 작업의 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82d38-103">Gets the information about an IotHub job.</span></span>

## <span data-ttu-id="82d38-104">구문</span><span class="sxs-lookup"><span data-stu-id="82d38-104">SYNTAX</span></span>

```
Get-AzIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82d38-105">설명</span><span class="sxs-lookup"><span data-stu-id="82d38-105">DESCRIPTION</span></span>
<span data-ttu-id="82d38-106">IotHub 작업에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82d38-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="82d38-107">가져오기 또는 내보내기 작업을 초기화할 때 IotHub 작업이 New-AzIotHubExportDevices 또는 New-AzIotHubImportDevices 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="82d38-107">An IotHub Job gets created when an import or export operation is initialized using the New-AzIotHubExportDevices or New-AzIotHubImportDevices commands.</span></span>
<span data-ttu-id="82d38-108">모든 작업을 나열하거나 작업 식별자에서 작업을 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82d38-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="82d38-109">예제</span><span class="sxs-lookup"><span data-stu-id="82d38-109">EXAMPLES</span></span>

### <span data-ttu-id="82d38-110">예제 1 모든 작업 나열</span><span class="sxs-lookup"><span data-stu-id="82d38-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="82d38-111">"myiothub"라는 IotHub에 대한 모든 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82d38-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="82d38-112">예제 2 특정 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="82d38-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="82d38-113">"myiothub"라는 IotHub의 식별자 "3630fc31-4caa-43e8-a232-ea0577221cb2"로 작업에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82d38-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="82d38-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="82d38-114">PARAMETERS</span></span>

### <span data-ttu-id="82d38-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82d38-115">-DefaultProfile</span></span>
<span data-ttu-id="82d38-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="82d38-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82d38-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="82d38-117">-JobId</span></span>
<span data-ttu-id="82d38-118">작업 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="82d38-118">The Job Identifier.</span></span> 

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

### <span data-ttu-id="82d38-119">-Name</span><span class="sxs-lookup"><span data-stu-id="82d38-119">-Name</span></span>
<span data-ttu-id="82d38-120">IoT 허브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82d38-120">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="82d38-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82d38-121">-ResourceGroupName</span></span>
<span data-ttu-id="82d38-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="82d38-122">Resource Group Name</span></span>

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

### <span data-ttu-id="82d38-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82d38-123">CommonParameters</span></span>
<span data-ttu-id="82d38-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="82d38-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82d38-125">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="82d38-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82d38-126">입력</span><span class="sxs-lookup"><span data-stu-id="82d38-126">INPUTS</span></span>

### <span data-ttu-id="82d38-127">System.String</span><span class="sxs-lookup"><span data-stu-id="82d38-127">System.String</span></span>

## <span data-ttu-id="82d38-128">출력</span><span class="sxs-lookup"><span data-stu-id="82d38-128">OUTPUTS</span></span>

### <span data-ttu-id="82d38-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="82d38-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="82d38-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="82d38-130">NOTES</span></span>

## <span data-ttu-id="82d38-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82d38-131">RELATED LINKS</span></span>
