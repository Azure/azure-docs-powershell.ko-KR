---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubexportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
ms.openlocfilehash: 3b04e0598897fb206ca781f4f19d9e8e2ec206dd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043817"
---
# <span data-ttu-id="85a38-101">New-AzIotHubExportDevice</span><span class="sxs-lookup"><span data-stu-id="85a38-101">New-AzIotHubExportDevice</span></span>

## <span data-ttu-id="85a38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85a38-102">SYNOPSIS</span></span>
<span data-ttu-id="85a38-103">새 장치 내보내기 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="85a38-103">Creates a new export devices job.</span></span>

## <span data-ttu-id="85a38-104">구문과</span><span class="sxs-lookup"><span data-stu-id="85a38-104">SYNTAX</span></span>

```
New-AzIotHubExportDevice [-ResourceGroupName] <String> [-Name] <String> [-ExportBlobContainerUri] <String>
 [-ExcludeKeys] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85a38-105">설명은</span><span class="sxs-lookup"><span data-stu-id="85a38-105">DESCRIPTION</span></span>
<span data-ttu-id="85a38-106">IotHub에 대 한 새 기기 내보내기 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="85a38-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="85a38-107">이렇게 하면 모든 장치가 지정 된 컨테이너로 내보내기 됩니다.</span><span class="sxs-lookup"><span data-stu-id="85a38-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="85a38-108">SAS URI를 생성 하는 방법에 대해서는 다음 문서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="85a38-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="85a38-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="85a38-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="85a38-110">예제의</span><span class="sxs-lookup"><span data-stu-id="85a38-110">EXAMPLES</span></span>

### <span data-ttu-id="85a38-111">예제 1에서는 내보내기 장치 요청을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="85a38-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

<span data-ttu-id="85a38-112">키를 제외 하 고 IotHub "myiothub"에 대 한 새 내보내기 장치 요청을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="85a38-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="85a38-113">변수</span><span class="sxs-lookup"><span data-stu-id="85a38-113">PARAMETERS</span></span>

### <span data-ttu-id="85a38-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85a38-114">-DefaultProfile</span></span>
<span data-ttu-id="85a38-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="85a38-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85a38-116">-ExcludeKeys</span><span class="sxs-lookup"><span data-stu-id="85a38-116">-ExcludeKeys</span></span>
<span data-ttu-id="85a38-117">키가 없는 장치를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85a38-117">Allows to export devices without keys.</span></span>

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

### <span data-ttu-id="85a38-118">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="85a38-118">-ExportBlobContainerUri</span></span>
<span data-ttu-id="85a38-119">Blob을 내보낼 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="85a38-119">The Uri to export the blob to.</span></span> 

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

### <span data-ttu-id="85a38-120">-이름</span><span class="sxs-lookup"><span data-stu-id="85a38-120">-Name</span></span>
<span data-ttu-id="85a38-121">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85a38-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="85a38-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85a38-122">-ResourceGroupName</span></span>
<span data-ttu-id="85a38-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="85a38-123">Resource Group Name</span></span>

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

### <span data-ttu-id="85a38-124">-확인</span><span class="sxs-lookup"><span data-stu-id="85a38-124">-Confirm</span></span>
<span data-ttu-id="85a38-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="85a38-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85a38-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85a38-126">-WhatIf</span></span>
<span data-ttu-id="85a38-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="85a38-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85a38-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85a38-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85a38-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85a38-129">CommonParameters</span></span>
<span data-ttu-id="85a38-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="85a38-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85a38-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85a38-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85a38-132">입력</span><span class="sxs-lookup"><span data-stu-id="85a38-132">INPUTS</span></span>

### <span data-ttu-id="85a38-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="85a38-133">System.String</span></span>

## <span data-ttu-id="85a38-134">출력</span><span class="sxs-lookup"><span data-stu-id="85a38-134">OUTPUTS</span></span>

### <span data-ttu-id="85a38-135">IotHub. PSIotHubJobResponse/. \*</span><span class="sxs-lookup"><span data-stu-id="85a38-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="85a38-136">상속자</span><span class="sxs-lookup"><span data-stu-id="85a38-136">NOTES</span></span>

## <span data-ttu-id="85a38-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85a38-137">RELATED LINKS</span></span>
