---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
ms.openlocfilehash: cc9bc7ef4171ea59f79f6e4687dddea4bc1dbae1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529809"
---
# <span data-ttu-id="95420-101">Remove-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="95420-101">Remove-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="95420-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95420-102">SYNOPSIS</span></span>
<span data-ttu-id="95420-103">Azure IoT Hub 인증서를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="95420-103">Deletes an Azure IoT Hub certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95420-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95420-104">SYNTAX</span></span>

### <span data-ttu-id="95420-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="95420-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95420-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="95420-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95420-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="95420-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95420-108">설명은</span><span class="sxs-lookup"><span data-stu-id="95420-108">DESCRIPTION</span></span>
<span data-ttu-id="95420-109">Azure IoT Hub의 CA 인증서에 대 한 자세한 설명은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="95420-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="95420-110">예제의</span><span class="sxs-lookup"><span data-stu-id="95420-110">EXAMPLES</span></span>

### <span data-ttu-id="95420-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="95420-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="95420-112">MyCertificate 삭제</span><span class="sxs-lookup"><span data-stu-id="95420-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="95420-113">변수</span><span class="sxs-lookup"><span data-stu-id="95420-113">PARAMETERS</span></span>

### <span data-ttu-id="95420-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="95420-114">-CertificateName</span></span>
<span data-ttu-id="95420-115">인증서 이름</span><span class="sxs-lookup"><span data-stu-id="95420-115">Name of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95420-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95420-116">-DefaultProfile</span></span>
<span data-ttu-id="95420-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95420-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95420-118">-Etag</span><span class="sxs-lookup"><span data-stu-id="95420-118">-Etag</span></span>
<span data-ttu-id="95420-119">인증서의 Etag</span><span class="sxs-lookup"><span data-stu-id="95420-119">Etag of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95420-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95420-120">-InputObject</span></span>
<span data-ttu-id="95420-121">인증서 개체</span><span class="sxs-lookup"><span data-stu-id="95420-121">Certificate Object</span></span>

```yaml
Type: PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95420-122">-이름</span><span class="sxs-lookup"><span data-stu-id="95420-122">-Name</span></span>
<span data-ttu-id="95420-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="95420-123">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95420-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95420-124">-PassThru</span></span>
<span data-ttu-id="95420-125">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="95420-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95420-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95420-126">-ResourceGroupName</span></span>
<span data-ttu-id="95420-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95420-127">Name of the Resource Group</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95420-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95420-128">-ResourceId</span></span>
<span data-ttu-id="95420-129">인증서 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="95420-129">Certificate Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95420-130">-확인</span><span class="sxs-lookup"><span data-stu-id="95420-130">-Confirm</span></span>
<span data-ttu-id="95420-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="95420-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95420-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95420-132">-WhatIf</span></span>
<span data-ttu-id="95420-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="95420-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95420-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95420-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95420-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95420-135">CommonParameters</span></span>
<span data-ttu-id="95420-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95420-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95420-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95420-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95420-138">입력</span><span class="sxs-lookup"><span data-stu-id="95420-138">INPUTS</span></span>

### <span data-ttu-id="95420-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="95420-139">System.String</span></span>

## <span data-ttu-id="95420-140">출력</span><span class="sxs-lookup"><span data-stu-id="95420-140">OUTPUTS</span></span>

### <span data-ttu-id="95420-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="95420-141">System.Boolean</span></span>

## <span data-ttu-id="95420-142">상속자</span><span class="sxs-lookup"><span data-stu-id="95420-142">NOTES</span></span>

## <span data-ttu-id="95420-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95420-143">RELATED LINKS</span></span>

