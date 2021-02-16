---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
ms.openlocfilehash: 3e30b7aa3d1e43844fc1fe53e860ee8b8c66f385
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200073"
---
# <span data-ttu-id="9867e-101">Remove-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="9867e-101">Remove-AzIotHubCertificate</span></span>

## <span data-ttu-id="9867e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9867e-102">SYNOPSIS</span></span>
<span data-ttu-id="9867e-103">Azure IoT Hub 인증서를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9867e-103">Deletes an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="9867e-104">구문</span><span class="sxs-lookup"><span data-stu-id="9867e-104">SYNTAX</span></span>

### <span data-ttu-id="9867e-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9867e-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9867e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9867e-106">InputObjectSet</span></span>
```
Remove-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9867e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9867e-107">ResourceIdSet</span></span>
```
Remove-AzIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9867e-108">설명</span><span class="sxs-lookup"><span data-stu-id="9867e-108">DESCRIPTION</span></span>
<span data-ttu-id="9867e-109">Azure IoT Hub의 CA 인증서에 대한 자세한 설명은 다음을 참조하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="9867e-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="9867e-110">예제</span><span class="sxs-lookup"><span data-stu-id="9867e-110">EXAMPLES</span></span>

### <span data-ttu-id="9867e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9867e-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="9867e-112">MyCertificate를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9867e-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="9867e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9867e-113">PARAMETERS</span></span>

### <span data-ttu-id="9867e-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="9867e-114">-CertificateName</span></span>
<span data-ttu-id="9867e-115">인증서의 이름</span><span class="sxs-lookup"><span data-stu-id="9867e-115">Name of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9867e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9867e-116">-DefaultProfile</span></span>
<span data-ttu-id="9867e-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9867e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9867e-118">-Etag</span><span class="sxs-lookup"><span data-stu-id="9867e-118">-Etag</span></span>
<span data-ttu-id="9867e-119">인증서의 Etag</span><span class="sxs-lookup"><span data-stu-id="9867e-119">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9867e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9867e-120">-InputObject</span></span>
<span data-ttu-id="9867e-121">인증서 개체</span><span class="sxs-lookup"><span data-stu-id="9867e-121">Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9867e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9867e-122">-Name</span></span>
<span data-ttu-id="9867e-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="9867e-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9867e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9867e-124">-PassThru</span></span>
<span data-ttu-id="9867e-125">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="9867e-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9867e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9867e-126">-ResourceGroupName</span></span>
<span data-ttu-id="9867e-127">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="9867e-127">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9867e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9867e-128">-ResourceId</span></span>
<span data-ttu-id="9867e-129">인증서 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="9867e-129">Certificate Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9867e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9867e-130">-Confirm</span></span>
<span data-ttu-id="9867e-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9867e-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9867e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9867e-132">-WhatIf</span></span>
<span data-ttu-id="9867e-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9867e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9867e-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9867e-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9867e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9867e-135">CommonParameters</span></span>
<span data-ttu-id="9867e-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9867e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9867e-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9867e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9867e-138">입력</span><span class="sxs-lookup"><span data-stu-id="9867e-138">INPUTS</span></span>

### <span data-ttu-id="9867e-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="9867e-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="9867e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9867e-140">System.String</span></span>

## <span data-ttu-id="9867e-141">출력</span><span class="sxs-lookup"><span data-stu-id="9867e-141">OUTPUTS</span></span>

### <span data-ttu-id="9867e-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9867e-142">System.Boolean</span></span>

## <span data-ttu-id="9867e-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9867e-143">NOTES</span></span>

## <span data-ttu-id="9867e-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9867e-144">RELATED LINKS</span></span>