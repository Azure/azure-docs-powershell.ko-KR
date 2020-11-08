---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BED3D3FE-D1E8-4857-A675-7B2670A129B2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 039afbea4d4eb6736cf3b0faebf189edef2d9c26
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046226"
---
# <span data-ttu-id="31cb2-101">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31cb2-101">New-AzureApplicationGateway</span></span>

## <span data-ttu-id="31cb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31cb2-102">SYNOPSIS</span></span>
<span data-ttu-id="31cb2-103">응용 프로그램 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31cb2-103">Creates an application gateway.</span></span>

## <span data-ttu-id="31cb2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31cb2-104">SYNTAX</span></span>

```
New-AzureApplicationGateway -Name <String> -VnetName <String>
 -Subnets <System.Collections.Generic.List`1[System.String]> [-InstanceCount <UInt32>] [-GatewaySize <String>]
 [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="31cb2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="31cb2-105">DESCRIPTION</span></span>
<span data-ttu-id="31cb2-106">**새-AzureApplicationGateway** cmdlet은 응용 프로그램 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31cb2-106">The **New-AzureApplicationGateway** cmdlet creates an application gateway.</span></span>

## <span data-ttu-id="31cb2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="31cb2-107">EXAMPLES</span></span>

### <span data-ttu-id="31cb2-108">예제 1: 응용 프로그램 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="31cb2-108">Example 1: Create an application gateway</span></span>
```
PS C:\> New-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork17" -Subnets @("Subnet01", "Subnet02", "Subnet03")
```

<span data-ttu-id="31cb2-109">이 명령은 ApplicationGateway06 라는 응용 프로그램 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31cb2-109">This command creates an application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="31cb2-110">이 명령은 VirtualNetwork17 및 지정 된 서브넷에서 게이트웨이를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="31cb2-110">The command deploys the gateway in VirtualNetwork17 and in the specified subnets.</span></span>

## <span data-ttu-id="31cb2-111">변수</span><span class="sxs-lookup"><span data-stu-id="31cb2-111">PARAMETERS</span></span>

### <span data-ttu-id="31cb2-112">-설명</span><span class="sxs-lookup"><span data-stu-id="31cb2-112">-Description</span></span>
<span data-ttu-id="31cb2-113">이 cmdlet가 응용 프로그램 게이트웨이에 할당 하는 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31cb2-113">Specifies a description that this cmdlet assigns to the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31cb2-114">--게이트웨이 크기</span><span class="sxs-lookup"><span data-stu-id="31cb2-114">-GatewaySize</span></span>
<span data-ttu-id="31cb2-115">이 cmdlet이 응용 프로그램 게이트웨이에 할당 하는 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31cb2-115">Specifies the size that this cmdlet assigns to the application gateway.</span></span>
<span data-ttu-id="31cb2-116">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="31cb2-116">Valid values are:</span></span>

- <span data-ttu-id="31cb2-117">Small</span><span class="sxs-lookup"><span data-stu-id="31cb2-117">Small</span></span>
- <span data-ttu-id="31cb2-118">높음이나</span><span class="sxs-lookup"><span data-stu-id="31cb2-118">Medium</span></span>
- <span data-ttu-id="31cb2-119">용량의</span><span class="sxs-lookup"><span data-stu-id="31cb2-119">Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31cb2-120">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="31cb2-120">-InstanceCount</span></span>
<span data-ttu-id="31cb2-121">이 cmdlet이 응용 프로그램 게이트웨이에 할당 하는 인스턴스 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31cb2-121">Specifies the number of instances that this cmdlet assigns to the application gateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31cb2-122">-이름</span><span class="sxs-lookup"><span data-stu-id="31cb2-122">-Name</span></span>
<span data-ttu-id="31cb2-123">새 application gateway의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31cb2-123">Specifies a name for the new application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31cb2-124">-프로필</span><span class="sxs-lookup"><span data-stu-id="31cb2-124">-Profile</span></span>
<span data-ttu-id="31cb2-125">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31cb2-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="31cb2-126">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="31cb2-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31cb2-127">-서브넷</span><span class="sxs-lookup"><span data-stu-id="31cb2-127">-Subnets</span></span>
<span data-ttu-id="31cb2-128">이 cmdlet이 응용 프로그램 게이트웨이를 배포 하는 서브넷의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31cb2-128">Specifies an array of subnets in which this cmdlet deploys the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31cb2-129">-VnetName</span><span class="sxs-lookup"><span data-stu-id="31cb2-129">-VnetName</span></span>
<span data-ttu-id="31cb2-130">이 cmdlet이 응용 프로그램 게이트웨이를 배포 하는 가상 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31cb2-130">Specifies the virtual network in which this cmdlet deploys the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31cb2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31cb2-131">CommonParameters</span></span>
<span data-ttu-id="31cb2-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31cb2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31cb2-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31cb2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31cb2-134">입력</span><span class="sxs-lookup"><span data-stu-id="31cb2-134">INPUTS</span></span>

### <span data-ttu-id="31cb2-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="31cb2-135">System.String</span></span>

## <span data-ttu-id="31cb2-136">출력</span><span class="sxs-lookup"><span data-stu-id="31cb2-136">OUTPUTS</span></span>

### <span data-ttu-id="31cb2-137">WindowsAzure의. i a m a 관리 응답</span><span class="sxs-lookup"><span data-stu-id="31cb2-137">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="31cb2-138">상속자</span><span class="sxs-lookup"><span data-stu-id="31cb2-138">NOTES</span></span>

## <span data-ttu-id="31cb2-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31cb2-139">RELATED LINKS</span></span>

[<span data-ttu-id="31cb2-140">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31cb2-140">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="31cb2-141">-AzureApplicationGateway 제거</span><span class="sxs-lookup"><span data-stu-id="31cb2-141">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="31cb2-142">시작-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31cb2-142">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="31cb2-143">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31cb2-143">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="31cb2-144">업데이트-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31cb2-144">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)
