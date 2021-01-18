---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubexportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
ms.openlocfilehash: 3b04e0598897fb206ca781f4f19d9e8e2ec206dd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495442"
---
# <span data-ttu-id="8dd94-101">New-AzIotHubExportDevice</span><span class="sxs-lookup"><span data-stu-id="8dd94-101">New-AzIotHubExportDevice</span></span>

## <span data-ttu-id="8dd94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dd94-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd94-103">새 내보내기 디바이스 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8dd94-103">Creates a new export devices job.</span></span>

## <span data-ttu-id="8dd94-104">구문</span><span class="sxs-lookup"><span data-stu-id="8dd94-104">SYNTAX</span></span>

```
New-AzIotHubExportDevice [-ResourceGroupName] <String> [-Name] <String> [-ExportBlobContainerUri] <String>
 [-ExcludeKeys] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dd94-105">설명</span><span class="sxs-lookup"><span data-stu-id="8dd94-105">DESCRIPTION</span></span>
<span data-ttu-id="8dd94-106">IotHub에 대한 새 내보내기 디바이스 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8dd94-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="8dd94-107">이렇게 하면 모든 디바이스를 지정된 컨테이너로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8dd94-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="8dd94-108">SAS URI를 생성하는 방법에 대한 다음 문서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8dd94-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="8dd94-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="8dd94-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="8dd94-110">예제</span><span class="sxs-lookup"><span data-stu-id="8dd94-110">EXAMPLES</span></span>

### <span data-ttu-id="8dd94-111">예제 1 내보내기 디바이스 요청을 발급합니다.</span><span class="sxs-lookup"><span data-stu-id="8dd94-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

<span data-ttu-id="8dd94-112">키를 제외한 IotHub "myiothub"에 대한 새 내보내기 디바이스 요청을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8dd94-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="8dd94-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8dd94-113">PARAMETERS</span></span>

### <span data-ttu-id="8dd94-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd94-114">-DefaultProfile</span></span>
<span data-ttu-id="8dd94-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8dd94-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8dd94-116">-ExcludeKeys</span><span class="sxs-lookup"><span data-stu-id="8dd94-116">-ExcludeKeys</span></span>
<span data-ttu-id="8dd94-117">키 없이 디바이스를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8dd94-117">Allows to export devices without keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd94-118">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="8dd94-118">-ExportBlobContainerUri</span></span>
<span data-ttu-id="8dd94-119">Blob을 내보낼 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="8dd94-119">The Uri to export the blob to.</span></span> 

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

### <span data-ttu-id="8dd94-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8dd94-120">-Name</span></span>
<span data-ttu-id="8dd94-121">IotHub의 이름</span><span class="sxs-lookup"><span data-stu-id="8dd94-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="8dd94-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dd94-122">-ResourceGroupName</span></span>
<span data-ttu-id="8dd94-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8dd94-123">Resource Group Name</span></span>

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

### <span data-ttu-id="8dd94-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8dd94-124">-Confirm</span></span>
<span data-ttu-id="8dd94-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8dd94-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dd94-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dd94-126">-WhatIf</span></span>
<span data-ttu-id="8dd94-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8dd94-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dd94-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8dd94-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dd94-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd94-129">CommonParameters</span></span>
<span data-ttu-id="8dd94-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8dd94-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd94-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8dd94-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd94-132">입력</span><span class="sxs-lookup"><span data-stu-id="8dd94-132">INPUTS</span></span>

### <span data-ttu-id="8dd94-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8dd94-133">System.String</span></span>

## <span data-ttu-id="8dd94-134">출력</span><span class="sxs-lookup"><span data-stu-id="8dd94-134">OUTPUTS</span></span>

### <span data-ttu-id="8dd94-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="8dd94-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="8dd94-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8dd94-136">NOTES</span></span>

## <span data-ttu-id="8dd94-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8dd94-137">RELATED LINKS</span></span>
