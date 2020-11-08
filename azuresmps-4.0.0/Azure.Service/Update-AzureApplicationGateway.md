---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C7F08804-E177-4BC5-8F0E-DEC1B467C4BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20cb37fbba8fd3789c0932f9ff1e9352334662e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045844"
---
# <span data-ttu-id="9dbbc-101">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9dbbc-101">Update-AzureApplicationGateway</span></span>

## <span data-ttu-id="9dbbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dbbc-102">SYNOPSIS</span></span>
<span data-ttu-id="9dbbc-103">응용 프로그램 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-103">Updates an application gateway.</span></span>

## <span data-ttu-id="9dbbc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9dbbc-104">SYNTAX</span></span>

```
Update-AzureApplicationGateway -Name <String> [-VnetName <String>]
 [-Subnets <System.Collections.Generic.List`1[System.String]>] [-InstanceCount <UInt32>]
 [-GatewaySize <String>] [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9dbbc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9dbbc-105">DESCRIPTION</span></span>
<span data-ttu-id="9dbbc-106">**업데이트-AzureApplicationGateway** cmdlet이 기존 application gateway를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-106">The **Update-AzureApplicationGateway** cmdlet updates an existing application gateway.</span></span>

## <span data-ttu-id="9dbbc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9dbbc-107">EXAMPLES</span></span>

### <span data-ttu-id="9dbbc-108">예제 1: 이름을 사용 하 여 응용 프로그램 게이트웨이 수정</span><span class="sxs-lookup"><span data-stu-id="9dbbc-108">Example 1: Modify an application gateway by using its name</span></span>
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork18" -Subnets @("Subnet05", "Subnet06")
```

<span data-ttu-id="9dbbc-109">첫 번째 명령은 ApplicationGateway06 이라는 응용 프로그램 게이트웨이를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-109">The first command stops the application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="9dbbc-110">가상 네트워크 또는 서브넷을 수정할 수 있으려면 먼저 응용 프로그램 게이트웨이를 중지 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-110">An application gateway must be stopped before you can modify the virtual network or subnets.</span></span>

<span data-ttu-id="9dbbc-111">두 번째 명령은 ApplicationGateway06 라는 응용 프로그램 게이트웨이의 가상 서브넷과 서브넷을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-111">The second command modifies the virtual subnet and subnets for the application gateway named ApplicationGateway06.</span></span>

### <span data-ttu-id="9dbbc-112">예제 2: 응용 프로그램 게이트웨이의 추가 속성 수정</span><span class="sxs-lookup"><span data-stu-id="9dbbc-112">Example 2: Modify additional properties of an application gateway</span></span>
```
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -InstanceCount 2 -GatewaySize "Large" -Description "Updated application gateway"
```

<span data-ttu-id="9dbbc-113">이 명령은 ApplicationGateway06 이라는 응용 프로그램 게이트웨이에 대 한 인스턴스 수, 게이트웨이 크기 및 설명을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-113">This command modifies the instance count, gateway size, and description for the application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="9dbbc-114">이 명령은 application gateway에 대 한 가상 네트워크 또는 서브넷을 수정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-114">This command does not modify the virtual network or subnets for the application gateway.</span></span>
<span data-ttu-id="9dbbc-115">따라서이 명령을 실행 하기 전에 응용 프로그램 게이트웨이를 중지할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-115">Therefore, you do not have to stop the application gateway before you run this command.</span></span>

### <span data-ttu-id="9dbbc-116">예제 3: 파이프라인을 사용 하 여 응용 프로그램 게이트웨이 수정</span><span class="sxs-lookup"><span data-stu-id="9dbbc-116">Example 3: Modify an application gateway by using the pipeline</span></span>
```
PS C:\> $ApplicationGateway = Get-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> $ApplicationGateway.GatewaySize = "Medium"
PS C:\> $ApplicationGateway | Update-AzureApplicationGateway
```

<span data-ttu-id="9dbbc-117">첫 번째 명령은 **Get-AzureApplicationGateway** cmdlet을 사용 하 여 ApplicationGateway06 라는 응용 프로그램 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-117">The first command gets the application gateway named ApplicationGateway06 by using the **Get-AzureApplicationGateway** cmdlet.</span></span>
<span data-ttu-id="9dbbc-118">명령이 $ApplicationGateway 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-118">The command stores it in the $ApplicationGateway variable.</span></span>

<span data-ttu-id="9dbbc-119">두 번째 명령은 값 매체에 대 한. m **size** 속성을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-119">The second command assigns the **GatewaySize** property the value Medium.</span></span>

<span data-ttu-id="9dbbc-120">마지막 명령은 현재 cmdlet에 업데이트 된 $ApplicationGateway을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-120">The final command passes the updated $ApplicationGateway to the current cmdlet.</span></span>

## <span data-ttu-id="9dbbc-121">변수</span><span class="sxs-lookup"><span data-stu-id="9dbbc-121">PARAMETERS</span></span>

### <span data-ttu-id="9dbbc-122">-설명</span><span class="sxs-lookup"><span data-stu-id="9dbbc-122">-Description</span></span>
<span data-ttu-id="9dbbc-123">이 cmdlet가 응용 프로그램 게이트웨이에 할당 하는 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-123">Specifies a description that this cmdlet assigns to the application gateway.</span></span>

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

### <span data-ttu-id="9dbbc-124">--게이트웨이 크기</span><span class="sxs-lookup"><span data-stu-id="9dbbc-124">-GatewaySize</span></span>
<span data-ttu-id="9dbbc-125">이 cmdlet이 응용 프로그램 게이트웨이에 할당 하는 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-125">Specifies the size that this cmdlet assigns to the application gateway.</span></span>
<span data-ttu-id="9dbbc-126">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-126">Valid values are:</span></span>

- <span data-ttu-id="9dbbc-127">Small</span><span class="sxs-lookup"><span data-stu-id="9dbbc-127">Small</span></span>
- <span data-ttu-id="9dbbc-128">높음이나</span><span class="sxs-lookup"><span data-stu-id="9dbbc-128">Medium</span></span>
- <span data-ttu-id="9dbbc-129">용량의</span><span class="sxs-lookup"><span data-stu-id="9dbbc-129">Large</span></span>

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

### <span data-ttu-id="9dbbc-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="9dbbc-130">-InstanceCount</span></span>
<span data-ttu-id="9dbbc-131">이 cmdlet이 응용 프로그램 게이트웨이에 할당 하는 인스턴스 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-131">Specifies the number of instances that this cmdlet assigns to the application gateway.</span></span>

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

### <span data-ttu-id="9dbbc-132">-이름</span><span class="sxs-lookup"><span data-stu-id="9dbbc-132">-Name</span></span>
<span data-ttu-id="9dbbc-133">이 cmdlet이 업데이트 하는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-133">Specifies the name of the application gateway that this cmdlet updates.</span></span>

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

### <span data-ttu-id="9dbbc-134">-프로필</span><span class="sxs-lookup"><span data-stu-id="9dbbc-134">-Profile</span></span>
<span data-ttu-id="9dbbc-135">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9dbbc-136">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9dbbc-137">-서브넷</span><span class="sxs-lookup"><span data-stu-id="9dbbc-137">-Subnets</span></span>
<span data-ttu-id="9dbbc-138">이 cmdlet이 응용 프로그램 게이트웨이를 배포 하는 서브넷의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-138">Specifies an array of subnets in which this cmdlet deploys the application gateway.</span></span>

<span data-ttu-id="9dbbc-139">응용 프로그램 게이트웨이가 실행 되는 동안에는 서브넷을 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-139">You cannot update subnets while the application gateway is running.</span></span>
<span data-ttu-id="9dbbc-140">응용 프로그램 게이트웨이를 중지 하려면 Stop-AzureApplicationGateway cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-140">To stop the application gateway, use the Stop-AzureApplicationGateway cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dbbc-141">-VnetName</span><span class="sxs-lookup"><span data-stu-id="9dbbc-141">-VnetName</span></span>
<span data-ttu-id="9dbbc-142">이 cmdlet이 응용 프로그램 게이트웨이를 배포 하는 가상 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-142">Specifies the virtual network in which this cmdlet deploys the application gateway.</span></span>

<span data-ttu-id="9dbbc-143">응용 프로그램 게이트웨이가 실행 되는 동안에는 가상 네트워크를 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-143">You cannot update a virtual network while the application gateway is running.</span></span>
<span data-ttu-id="9dbbc-144">응용 프로그램 게이트웨이를 중지 하려면 **stop-AzureApplicationGateway** 를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-144">To stop the application gateway, use **Stop-AzureApplicationGateway**.</span></span>

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

### <span data-ttu-id="9dbbc-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dbbc-145">CommonParameters</span></span>
<span data-ttu-id="9dbbc-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dbbc-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dbbc-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dbbc-148">입력</span><span class="sxs-lookup"><span data-stu-id="9dbbc-148">INPUTS</span></span>

### <span data-ttu-id="9dbbc-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9dbbc-149">System.String</span></span>

## <span data-ttu-id="9dbbc-150">출력</span><span class="sxs-lookup"><span data-stu-id="9dbbc-150">OUTPUTS</span></span>

### <span data-ttu-id="9dbbc-151">WindowsAzure의. i a m a 관리 응답</span><span class="sxs-lookup"><span data-stu-id="9dbbc-151">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="9dbbc-152">상속자</span><span class="sxs-lookup"><span data-stu-id="9dbbc-152">NOTES</span></span>

## <span data-ttu-id="9dbbc-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9dbbc-153">RELATED LINKS</span></span>

[<span data-ttu-id="9dbbc-154">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9dbbc-154">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="9dbbc-155">새 AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9dbbc-155">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="9dbbc-156">-AzureApplicationGateway 제거</span><span class="sxs-lookup"><span data-stu-id="9dbbc-156">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="9dbbc-157">시작-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9dbbc-157">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="9dbbc-158">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9dbbc-158">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)
