---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothubimportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
ms.openlocfilehash: f2a2daebcb77746ae087fe527245376963fade5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956155"
---
# <span data-ttu-id="755fb-101">New-AzIotHubImportDevice</span><span class="sxs-lookup"><span data-stu-id="755fb-101">New-AzIotHubImportDevice</span></span>

## <span data-ttu-id="755fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="755fb-102">SYNOPSIS</span></span>
<span data-ttu-id="755fb-103">새 가져오기 디바이스 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="755fb-103">Creates a new import devices job.</span></span>

## <span data-ttu-id="755fb-104">구문</span><span class="sxs-lookup"><span data-stu-id="755fb-104">SYNTAX</span></span>

```
New-AzIotHubImportDevice [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="755fb-105">설명</span><span class="sxs-lookup"><span data-stu-id="755fb-105">DESCRIPTION</span></span>
<span data-ttu-id="755fb-106">IotHub에 대한 새 가져오기 디바이스 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="755fb-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="755fb-107">이렇게 하면 지정된 컨테이너에서 IotHub로 모든 디바이스를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="755fb-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="755fb-108">SAS URI를 생성하는 방법에 대한 다음 문서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="755fb-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="755fb-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="755fb-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="755fb-110">예제</span><span class="sxs-lookup"><span data-stu-id="755fb-110">EXAMPLES</span></span>

### <span data-ttu-id="755fb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="755fb-111">Example 1</span></span>
```
PS C:\> New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="755fb-112">IotHub "myiothub"에 대한 새 가져오기 디바이스 요청을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="755fb-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="755fb-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="755fb-113">PARAMETERS</span></span>

### <span data-ttu-id="755fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="755fb-114">-DefaultProfile</span></span>
<span data-ttu-id="755fb-115">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="755fb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="755fb-116">-InputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="755fb-116">-InputBlobContainerUri</span></span>
<span data-ttu-id="755fb-117">FileUpload용 입력 Blob Container Uri</span><span class="sxs-lookup"><span data-stu-id="755fb-117">Input Blob Container Uri for FileUpload</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="755fb-118">-Name</span><span class="sxs-lookup"><span data-stu-id="755fb-118">-Name</span></span>
<span data-ttu-id="755fb-119">IotHub의 이름</span><span class="sxs-lookup"><span data-stu-id="755fb-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="755fb-120">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="755fb-120">-OutputBlobContainerUri</span></span>
<span data-ttu-id="755fb-121">출력을 작성할 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="755fb-121">The Uri to write the output to.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="755fb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="755fb-122">-ResourceGroupName</span></span>
<span data-ttu-id="755fb-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="755fb-123">Resource Group Name</span></span>

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

### <span data-ttu-id="755fb-124">-확인</span><span class="sxs-lookup"><span data-stu-id="755fb-124">-Confirm</span></span>
<span data-ttu-id="755fb-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="755fb-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="755fb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="755fb-126">-WhatIf</span></span>
<span data-ttu-id="755fb-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="755fb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="755fb-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="755fb-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="755fb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="755fb-129">CommonParameters</span></span>
<span data-ttu-id="755fb-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="755fb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="755fb-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="755fb-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="755fb-132">입력</span><span class="sxs-lookup"><span data-stu-id="755fb-132">INPUTS</span></span>

### <span data-ttu-id="755fb-133">System.String</span><span class="sxs-lookup"><span data-stu-id="755fb-133">System.String</span></span>

## <span data-ttu-id="755fb-134">출력</span><span class="sxs-lookup"><span data-stu-id="755fb-134">OUTPUTS</span></span>

### <span data-ttu-id="755fb-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="755fb-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="755fb-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="755fb-136">NOTES</span></span>

## <span data-ttu-id="755fb-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="755fb-137">RELATED LINKS</span></span>
