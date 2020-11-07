---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubimportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
ms.openlocfilehash: 50f0652f477edad13fb661683b1ee2f2f13fef9d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876730"
---
# <span data-ttu-id="2b7c8-101">New-AzIotHubImportDevice</span><span class="sxs-lookup"><span data-stu-id="2b7c8-101">New-AzIotHubImportDevice</span></span>

## <span data-ttu-id="2b7c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b7c8-102">SYNOPSIS</span></span>
<span data-ttu-id="2b7c8-103">새 장치 가져오기 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-103">Creates a new import devices job.</span></span>

## <span data-ttu-id="2b7c8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b7c8-104">SYNTAX</span></span>

```
New-AzIotHubImportDevice [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b7c8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2b7c8-105">DESCRIPTION</span></span>
<span data-ttu-id="2b7c8-106">IotHub에 대 한 새 장치 가져오기 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="2b7c8-107">이렇게 하면 지정 된 컨테이너에서 모든 장치를 IotHub로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="2b7c8-108">SAS URI를 생성 하는 방법에 대해서는 다음 문서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="2b7c8-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="2b7c8-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="2b7c8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2b7c8-110">EXAMPLES</span></span>

### <span data-ttu-id="2b7c8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2b7c8-111">Example 1</span></span>
```
PS C:\> New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="2b7c8-112">IotHub "myiothub"에 대 한 새 가져오기 장치 요청을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="2b7c8-113">변수</span><span class="sxs-lookup"><span data-stu-id="2b7c8-113">PARAMETERS</span></span>

### <span data-ttu-id="2b7c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b7c8-114">-DefaultProfile</span></span>
<span data-ttu-id="2b7c8-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2b7c8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b7c8-116">-InputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="2b7c8-116">-InputBlobContainerUri</span></span>
<span data-ttu-id="2b7c8-117">FileUpload에 대 한 입력 Blob 컨테이너 Uri</span><span class="sxs-lookup"><span data-stu-id="2b7c8-117">Input Blob Container Uri for FileUpload</span></span>

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

### <span data-ttu-id="2b7c8-118">-이름</span><span class="sxs-lookup"><span data-stu-id="2b7c8-118">-Name</span></span>
<span data-ttu-id="2b7c8-119">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="2b7c8-120">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="2b7c8-120">-OutputBlobContainerUri</span></span>
<span data-ttu-id="2b7c8-121">출력을 쓸 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-121">The Uri to write the output to.</span></span> 

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

### <span data-ttu-id="2b7c8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b7c8-122">-ResourceGroupName</span></span>
<span data-ttu-id="2b7c8-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2b7c8-123">Resource Group Name</span></span>

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

### <span data-ttu-id="2b7c8-124">-확인</span><span class="sxs-lookup"><span data-stu-id="2b7c8-124">-Confirm</span></span>
<span data-ttu-id="2b7c8-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b7c8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b7c8-126">-WhatIf</span></span>
<span data-ttu-id="2b7c8-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b7c8-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b7c8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b7c8-129">CommonParameters</span></span>
<span data-ttu-id="2b7c8-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b7c8-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b7c8-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b7c8-132">입력</span><span class="sxs-lookup"><span data-stu-id="2b7c8-132">INPUTS</span></span>

### <span data-ttu-id="2b7c8-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2b7c8-133">System.String</span></span>

## <span data-ttu-id="2b7c8-134">출력</span><span class="sxs-lookup"><span data-stu-id="2b7c8-134">OUTPUTS</span></span>

### <span data-ttu-id="2b7c8-135">IotHub. PSIotHubJobResponse/. \*</span><span class="sxs-lookup"><span data-stu-id="2b7c8-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="2b7c8-136">상속자</span><span class="sxs-lookup"><span data-stu-id="2b7c8-136">NOTES</span></span>

## <span data-ttu-id="2b7c8-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b7c8-137">RELATED LINKS</span></span>
